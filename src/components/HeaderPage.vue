<template>
  <nav class="navbar navbar-expand-lg bg-nav">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src=../assets/logo1.png alt="">
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="collapse navbar-collapse justify-content-between"
        id="navbarSupportedContent"
      >
        <ul class="navbar-nav ml-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active majalla24" aria-current="page" href="#"
              >مزايا كتيبنا</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link active majalla24" aria-current="page" href="#"
              >لماذا تحصل عليه</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link active majalla24" aria-current="page" href="#"
              >أراء العملاء</a
            >
          </li>
        </ul>
        <div class="d-flex">
          <a href="http://" target="_blank" rel="noopener noreferrer">
            <button
              type="button"
              class="btn btn-light majalla24 py-2 px-4 hover"
            >
              اطلب بطاقة تهنئة
            </button></a
          >
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
export default {};
</script>

<style scoped>
@import "@/assets/css/styles.css";

.navbar {
  background-color: #c7ecec;
}
.navbar-brand img {
  width: 180px;
}
.nav-item {
  padding-left: 20px;
}
.navbar-nav {
  padding-right: 20%;
}
</style>