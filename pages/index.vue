<template>
  <div class="home">
    <section class="hero">
      <main class="self-center flex flex-col flex-1 items-center justify-center" style="height: 100%">
        <section class="self-center flex flex-col flex-1 items-center justify-center">
          <img src="icon.png" width="120" alt="" />
          <h1 class="title text-center" style="color: #fff !important">UPC GIFT - PASAY</h1>
          <h6 class="text-center max-w-5xl mx-auto" style="color: #fff !important">
            "A grace abounding church that everyone would want to join and be a part of. Seeking and saving God's lost
            children in Pasay City; Distributing His gifts to everyone, gloryfing the name of the Lord Jesus Christ in
            the process."
          </h6>
        </section>
      </main>
    </section>
    <main>
      <section class="mt-5">
        <h3 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">About Us</h3>
        <p class="max-w-5xl mx-auto">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque pariatur nemo possimus, libero beatae eligendi
          dolor explicabo laboriosam error natus aliquam tempora assumenda animi illum voluptas sed aut! Error,
          accusantium.
        </p>
      </section>

      <section class="mt-8">
        <h3 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">Latest post</h3>
        <posts post-type="blog" :amount="1" />
        <posts post-type="projects" :amount="1" />
      </section>
    </main>
    <footer class="max-w-5xl mx-auto py-3">&copy; UPC GIFT - PASAY 2021</footer>
  </div>
</template>

<style>
.home {
  width: 100%;
}
.hero {
  background-image: url('static/home-bg.jpg');
  background-attachment: fixed;
  background-size: cover;
  background-position: center;
  height: 80vh;
}
</style>
