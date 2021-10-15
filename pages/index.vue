<template>
  <div class="home">
    <section class="hero">
      <main class="self-center flex flex-col flex-1 items-center justify-center" style="height: 100%">
        <section class="self-center flex flex-col flex-1 items-center justify-center">
          <!-- <img src="icon.png" width="120" alt="" /> -->
          <h1 class="title home-title text-center" style="color: #fff !important">WELCOME TO GIFT CHURCH!</h1>
          <h4 class="text-center max-w-5xl mx-auto" style="color: #fff !important">
            "One Lord, One faith, One Baptism" - Ephesians 4:5
          </h4>
          <!-- <a class="mt-3" style="color: #fff" href="https://www.facebook.com/GIFTPASAY" target="_blank">
            <span style="font-size: 2rem" class="material-icons">facebook</span>
          </a> -->
        </section>
      </main>
    </section>
    <main style="padding-bottom: 0">
      <section class="mt-5 text-center pt-10 pb-20 vision-mission">
        <h2 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">VISION & MISSION</h2>
        <h5 class="max-w-5xl mx-auto">
          "A grace abounding church everyone would want to join and be apart of. Seeking and saving God's lost children
          in Pasay City; Distributing His GIFTS to everyone, glorifying the name of The Lord Jesus Christ in the
          process."
        </h5>
      </section>

      <div class="divider"></div>

      <section class="mt-20">
        <h3 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">SCRIPTURE STUDY</h3>
        <posts post-type="blog" :amount="2" />
      </section>
    </main>
    <section class="contact-section">
      <h3>REACH US</h3>
      <span>0912.345.6789</span>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15447.651667647862!2d120.9964069!3d14.5469723!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x2d283632efa6ae9a!2sUnited%20Pentecostal%20Church%20Pasay%20City%20-%20Libertad!5e0!3m2!1sen!2sph!4v1634306107610!5m2!1sen!2sph"
        style="border: 0"
        allowfullscreen=""
        class="google-map"
        loading="lazy"
      ></iframe>
    </section>
  </div>
</template>

<style lang="postcss">
.home {
  width: 100%;
}
.hero {
  background-image: url('static/home-bg.jpg');
  background-attachment: fixed;
  background-size: cover;
  background-position: center;
  height: 95vh;
}

.contact-section {
  background-image: url('static/contact.jpg');
  background-attachment: fixed;
  background-size: cover;
  background-position: center;
  height: 50vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 3rem;
  padding: 1.5rem;
}

.contact-section h3,
.contact-section span {
  color: #fff;
}

.google-map {
  max-width: 100%;
  width: 500px;
  height: 300px;
  margin: auto;
  margin-top: 1rem;
  @media screen and (max-width: 426px) {
    /* width: 325px; */
    height: 200px;
  }
  border-radius: 5px;
}

.home-title {
  font-size: 3.5rem;
  line-height: 3.5rem;
}

.divider {
  max-width: 100%;
  width: 10rem;
  margin: 0 auto;
  border-bottom: 1px solid var(--color-primary-600);
}
</style>
