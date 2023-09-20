<template>
  <section class="box-form">
    <div class="container py-5">
      <div class="text-center">
        <h3 class="text-white majallab36 py-5">أطلب الكتيب بدون تردد</h3>
      </div>
      <div class="row d-flex align-items-center justify-content-center">
        <div class="col-lg-6 col-md-12 text-white">
          <div class="d-flex py-3">
            <h2 class="majallab40 size">
              زد مبيعات متجرك %500 <br />بهذه الاستراتيجيات
              <img src="../assets/icon-hero.png" alt="" width="50px" />
            </h2>
          </div>
          <p class="majalla28">
            أسرار لا تخبرك بها شركات التسويق سوف تجدها في كتيبنا، <br />
            كن أول من يحصل عليه وستجني ثماره بإذن الله
          </p>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="black my-5">
            <h5 class="majallab24 py-2">أطلب نسختك من الكتيب الآن</h5>
            <p class="text-muted majalla18">
              سجل بياناتك واستفيد من خدماتنا الرائعة
            </p>
            <div
              class="row box-input d-flex align-items-center justify-content-center"
            >
              <div class="col-12">
                <form @submit.prevent="postData">
                  <div class="my-2">
                    <input
                      type="text"
                      class="form-control majalla20"
                      v-model="name"
                      placeholder="ادخل اسمك هنا"
                    />
                  </div>
                  <div class="my-2">
                    <input
                      type="email"
                      class="form-control majalla20"
                      v-model="email"
                      placeholder="ايميلك الشخصي"
                    />
                  </div>
                  <div class="mt-2 pb-2">
                    <input
                      type="text"
                      class="form-control majalla20"
                      v-model="phone"
                      placeholder="رقم الموبايل"
                    />
                  </div>
                  <input
                    type="checkbox"
                    class="form-check-input"
                    id="exampleCheck1"
                  />
                  <span class="text-muted majalla18">
                    تلقي الاشعارات بشأن التحديثات حول الكتيب
                  </span>

                  <div class="my-4 but">
                    <button
                      type="submit"
                      class="btn btn-primary majalla20 blod-none"
                      :disabled="isSubmitting"
                    >
                      {{ isSubmitting ? "جاري الإرسال..." : "أطلب نسختك الآن" }}
                    </button>
                    <!-- عرض الرسالة عندما يكون uploading هو true -->
                    <div v-if="uploading" class="text-success majalla18">
                      {{ successMessage }}
                    </div>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      name: "",
      email: "",
      phone: "",
      isSubmitting: false,
      uploading: false,
      successMessage: "",
    };
  },
  methods: {
    async postData() {
      try {
        this.isSubmitting = true;
        const response = await axios.post(
          "http://192.168.3.103/celebration/public/api/send-email-pdf",
          {
            name: this.name,
            email: this.email,
            phone: this.phone,
          }
        );
        console.log("Data sent successfully:", response.data);

        // Clear the input fields after successful submission
        this.name = "";
        this.email = "";
        this.phone = "";

        this.uploading = true;

        // Show a success message
        this.successMessage = "تم الاسال بنجاح";

        // You can reset the success message after a certain time if needed
        setTimeout(() => {
          this.isSubmitting = false;
          this.uploading = false;
          this.successMessage = "";
        }, 5000); // Clear the message after 5 seconds (adjust the time as needed)
      } catch (error) {
        console.error("Error sending data:", error);
        // Handle errors as needed
      }
    },
  },
};
</script>