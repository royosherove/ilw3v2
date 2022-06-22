<script type="module" lang="ts">
  const navigation = [
  { name: 'בית', href: '/', current: false },
  { name: 'הקלטות', href: '/videos', current: false },
  { name: 'אודות', href: '/about', current: false },
  { name: 'הצעת אירוח', href: '/host', current: false },
  { name: 'הגשת הרצאה', href: '/submit', current: false },
  { name: 'אירועים קרובים', href: '/events', current: false },
  { name: 'שידור חי', href: '/live', current: false },
]

function switchPage(newPageName:string){
   navigation.forEach(n=>n.current=(n.name===newPageName)) ;
   menuOpen=false;
}

let menuOpen = false;
</script>
<!-- This example requires Tailwind CSS v2.0+ -->
<nav class="bg-gray-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <div class="hidden sm:block sm:ml-6">
            <div class="flex space-x-4">
                {#each navigation as nav}
                    <a href={nav.href} 
                    class="{(nav.current? 'bg-gray-900 text-white' :'hover:bg-gray-700 text-gray-300') +  ' px-3 py-2 rounded-md text-sm font-medium'}"
                    on:click={()=>switchPage(nav.name)}
                    >
                    {nav.name}
                </a>
                {/each}
            </div>
          </div>
        </div>
        <div class="hidden sm:ml-6 sm:block">
          <div class="flex items-center">
  
              <!--
                Dropdown menu, show/hide based on menu state.
  
                Entering: "transition ease-out duration-100"
                  From: "transform opacity-0 scale-95"
                  To: "transform opacity-100 scale-100"
                Leaving: "transition ease-in duration-75"
                  From: "transform opacity-100 scale-100"
                  To: "transform opacity-0 scale-95"
              -->
          </div>
        </div>
        <div class="-mr-2 flex sm:hidden">
          <!-- Mobile menu button -->
          <button type="button" 
            class="
                inline-flex items-center justify-center p-2 
                rounded-md text-gray-400 hover:text-white hover:bg-gray-700 
                focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" 
                aria-controls="mobile-menu" 
                aria-expanded="false"
                on:click={()=>menuOpen=!menuOpen}
                >
            <span class="sr-only">Open main menu</span>
            <!--
              Icon when menu is closed.
  
              Heroicon name: outline/menu
  
              Menu open: "hidden", Menu closed: "block"
            -->
            <svg class="block h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <!--
              Icon when menu is open.
  
              Heroicon name: outline/x
  
              Menu open: "block", Menu closed: "hidden"
            -->
            <svg class="hidden h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>
  
    <!-- Mobile menu, show/hide based on menu state. -->
    {#if menuOpen}
    <div class="sm:hidden" id="mobile-menu">
      <div class="px-2 pt-2 pb-3 space-y-1">
        {#each navigation as nav}
            <a href={nav.href} 
            class="{(nav.current? 'bg-gray-900 text-white' :'hover:bg-gray-700 text-gray-300') +  ' block px-3 py-2 rounded-md text-sm font-medium'}"
            on:click={()=>switchPage(nav.name)}
            >
            {nav.name}</a>
            <!-- <a href="#" class="bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium">Dashboard</a> -->
        {/each}
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
      </div>
      <div class="pt-4  border-t border-gray-700">
      </div>
    </div>
    {/if}
  </nav>
  