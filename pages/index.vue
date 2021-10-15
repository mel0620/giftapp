<template>
  <div class="home">
    <section class="hero">
      <main class="self-center flex flex-col flex-1 items-center justify-center" style="height: 100%">
        <section class="self-center flex flex-col flex-1 items-center justify-center">
          <!-- <img src="icon.png" width="120" alt="" /> -->
          <h1 class="title home-title text-center" style="color: #fff !important">WELCOME TO GIFT CHURCH!</h1>
          <h4 class="text-center max-w-5xl mx-auto" style="color: #fff !important">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda libero id, quidem blanditiis dolore
            omnis.
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

      <!-- <div class="divider"></div> -->

      <section class="mt-8">
        <h3 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">LATEST POSTS</h3>
        <posts post-type="blog" :amount="2" />
      </section>
    </main>
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

.home-title {
  font-size: 3.5rem;
  line-height: 3.5rem;
}

.divider {
  max-width: 64rem;
  width: 100%;
  margin: 0 auto;
  border-bottom: 1px solid var(--color-primary);
}
</style>
