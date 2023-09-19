<template>
  <section class="box-form">
    <div class="container py-5">
      <div class="text-center">
        <h3 class="text-white py-5">أطلب الكتيب بدون تردد</h3>
      </div>
      <div class="row d-flex align-items-center justify-content-center">
        <div class="col-lg-6 col-md-12 text-white">
          <div class="d-flex py-3">
            <h2 class="">
              زد مبيعات متجرك %500 <br />بهذه الاستراتيجيات
              <img src="../assets/icon-hero.png" alt="" width="50px" />
            </h2>
          </div>
          <p>
            أسرار لا تخبرك بها شركات التسويق سوف تجدها في كتيبنا، <br />
            كن أول من يحصل عليه وستجني ثماره بإذن الله
          </p>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="black my-5">
            <h5 class="font-Regular14py-2">أطلب نسختك من الكتيب الآن</h5>
            <p class="text-muted">سجل بياناتك واستفيد من خدماتنا الرائعة</p>
            <div
              class="row box-input d-flex align-items-center justify-content-center"
            >
              <div class="col-12">
                <form @submit.prevent="postData">
                  <div class="my-2">
                    <input
                      type="text"
                      class="form-control"
                      v-model="name"
                      placeholder="ادخل اسمك هنا"
                    />
                  </div>
                  <div class="my-2">
                    <input
                      type="text"
                      class="form-control"
                      v-model="name"
                      placeholder="ادخل اسمك هنا"
                    />
                  </div>
                  <div class="mt-2 pb-3">
                    <input
                      type="email"
                      class="form-control"
                      v-model="email"
                      placeholder="ايميلك الشخصي"
                    />
                  </div>
                  <input
                    type="checkbox"
                    class="form-check-input"
                    id="exampleCheck1"
                  />  <span class="text-muted"> تلقي الاشعارات بشأن التحديثات حول الكتيب</span>

                  <div class="my-4 but">
                    <button
                      type="submit"
                      class="btn btn-primary font-Regular14 blod-none"
                    >
                      أطلب هديتك الفورية
                    </button>
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

