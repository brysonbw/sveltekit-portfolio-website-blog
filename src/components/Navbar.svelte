<script lang="ts">
  import avatarImage from '../components/images/bryson-avatar.jpg'
  let navbarOpen = false
   
</script>

<div class="fixed top-0 w-full z-30 clearNav md:bg-opacity-90 transition duration-300 ease-in-out">
    <div class="flex flex-col max-w-6xl px-4 mx-auto md:items-center md:justify-between md:flex-row md:px-6 lg:px-8 bg-[#171717]">
      <div class="flex flex-row items-center justify-between p-2">
       
          <img
            
            src={avatarImage}
            class='borderCircle'
            height={40}
            width={40}
            alt={'bryson-avatar'}
          />
        
        <p class="md:ml-2">DevBryson</p>
        <button
          class="text-white cursor-pointer leading-none px-3 py-1 md:hidden outline-none focus:outline-none "
          type="button"
          aria-label="button"
          on:click={() => (navbarOpen = !navbarOpen)}
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="#ffffff"
            stroke-width="2"
            stroke-Linecap="round"
            stroke-Linejoin="round"
            class="feather feather-menu"
          >
            <line x1="3" y1="12" x2="21" y2="12"></line>
            <line x1="3" y1="6" x2="21" y2="6"></line>
            <line x1="3" y1="18" x2="21" y2="18"></line>
          </svg>
        </button>
      </div>
      <div
        class={
          "md:flex flex-grow items-center" +
          (navbarOpen ? " flex" : " hidden")
        }
      >
        <nav class="flex-col flex-grow ">
          <ul class="flex flex-grow justify-end flex-wrap items-center">
            <li>
             
                <a   href="/" class="font-medium text-[#bca8ff] hover:underline px-5 py-3 flex items-center transition duration-150 ease-in-out">Home</a>
            
            </li>
            
            <li>
             
                <a href="/portfolio"  class="font-medium text-[#bca8ff] hover:underline px-5 py-3 flex items-center transition duration-150 ease-in-out">Portfolio</a>
             
            </li>

            <li>
             
              <a href="/blog"  class="font-medium text-[#bca8ff] hover:underline px-5 py-3 flex items-center transition duration-150 ease-in-out">Blog</a>
           
          </li>

           
            
          </ul>
        </nav>
      </div>
    </div>
  </div>

  <style>
     .borderCircle {
    border-radius: 9999px;
  }
  </style>