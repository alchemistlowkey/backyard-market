<script>
    import { faTwitter, faInstagram, faFacebook, faWhatsapp, faTiktok } from "@fortawesome/free-brands-svg-icons";
    import { Fa } from "svelte-fa";
    import logo from "$lib/images/logo.png"
</script>

<footer class="footer bg-base-200 p-20 ps-40 justify-between text-[#0D494E]">
  <aside class="md:place-self-center md:justify-self-end">
    <img src={logo} alt="An alt text" class="w-44 h-44" />
    
  </aside>
    <nav>
      <h6 class="footer-title">Services</h6>
      <a href="/" class="link link-hover">Market Errands</a>
      <a href="/" class="link link-hover">Local Snacks</a>
      <a href="/" class="link link-hover">Ram Sharing</a>
      <a href="/" class="link link-hover">Event Packs</a>
    </nav>
    <nav>
      <h6 class="footer-title">Company</h6>
      <a href="/" class="link link-hover">About us</a>
      <a href="/" class="link link-hover">Contact us</a>
      <a href="/" class="link link-hover">Location</a>
      <a href="/" class="link link-hover">Delivery</a>
    </nav>
    <nav class="md:place-self-center md:justify-self-end">
      <div class="flex flex-row">
        <a href="https://x.com/Backyard__Mt" class="btn btn-ghost text-3xl hover:bg-green-100 m-1">
          <Fa icon={faTwitter} />
        </a>
        <a href="https://www.instagram.com/backyard__market._/" class="btn btn-ghost text-3xl hover:bg-green-100 m-1">
          <Fa icon={faInstagram} />
        </a>
        <a href="https://web.facebook.com/profile.php?id=100085630810360" class="btn btn-ghost text-3xl hover:bg-green-100 m-1">
          <Fa icon={faFacebook} />
        </a>
        <a href="https://www.tiktok.com/@backyardmarket" class="btn btn-ghost text-3xl hover:bg-green-100 m-1">
          <Fa icon={faTiktok} />
        </a>     
      </div>
    </nav>
  </footer>

  <footer class="footer justify-center bg-[#f5fffe] text-[#0D494E] p-5">
    <aside class="footer mx-auto max-w-lg justify-center p-2">
      <p>©2024 - All right reserved by Backyard Market</p>
    </aside>
  </footer>

<style></style>