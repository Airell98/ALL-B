<template>
  <div class="wrapper">
    <div class="content-center">
      <div class="the-header">
        <div class="the-header-text">
          <h1>Junior Full Stack Developer Class</h1>
        </div>
      </div>
      <div class="the-image">
        <img
          src="https://images.unsplash.com/photo-1531482615713-2afd69097998?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80"
          alt="image1"
          class="image-fullStack"
        />
      </div>
      <div class="the-desc">
        <p class="first-paragraph">
          <span style="font-weight: bolder"
            >Junior Full Stack Developer Class</span
          >
          merupakan kelas intensif untuk menjadi seorang junior full stack
          developer. Kelas ini akan berlangsung selama 16 minggu dengan sistem
          pembelajaran live online secara langsung melalui zoom, sehingga
          peserta dapat berinteraksi langsung dengan instruktur selama
          pembelajaran berlangsung. Dalam 1 pekan akan ada 3 kali pertemuan
          selama 1 - 2 jam per pertemuannya dan peserta akan diberikan challenge
          disetiap akhir pertemuan. Silabus pembelajaran disusun khusus untuk
          segala background pendidikan yang bahkan belum tau sama sekali tentang
          pemrograman. Target utama dari pembelajaran ini yaitu peserta dengan
          secara mandiri membangun software maupun web yang diinginkan, peserta
          dapat dengan mudah mengembangkan diri dengan mempelajari bahasa maupun
          teknologi baru dalam dunia pemrograman, kemudian peserta memiliki
          skill dan experience yang mumpuni dan dapat langsung terjun untuk
          bekerja di perusahaan developer.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$seribuDuaRatus: 1200px;
$screen-lg-min: 992px;
$screen-md-min: 775px;
$screen-sm-min: 576px;
$empatRatusLimaPuluh: 450px;
.content-center {
  text-align: center;
  .the-header {
    margin-top: 20px;
    .the-header-text {
      color: white;
      font-family: "Tienne", serif;
      h1 {
        @media only screen and (max-width: $seribuDuaRatus) {
          font-size: 30px;
        }
        @media only screen and (max-width: $screen-lg-min) {
          font-size: 24px;
        }
        @media only screen and (max-width: $screen-md-min) {
          font-size: 18px;
        }
         @media only screen and (max-width: $screen-sm-min) {
          font-size: 13px;
        }
      }
    }
  }
  .the-image {
    margin-top: 20px;
    .image-fullStack {
      width: 60%;
    }
  }
  .the-desc {
    color: white;
    width: 65%;
    margin: auto;
    .first-paragraph {
      margin-top: 40px;
      font-size: 20px;
      text-align: justify;
      letter-spacing: 1px;
       
        // @media only screen and (max-width: $screen-lg-min) {
        //   font-size: 24px;
        // }
        @media only screen and (max-width: $screen-md-min) {
          font-size: 16px;
           letter-spacing: 0;
            line-height: 2;
        }
         @media only screen and (max-width: $screen-sm-min) {
          font-size: 13px;
        }
         @media only screen and (max-width: $empatRatusLimaPuluh) {
          font-size: 10px;
          
        }
    }
  }
}
</style>