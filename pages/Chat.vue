<template>
  <div class="font-sans antialiased h-screen flex">

    <div class="bg-white border-gray-400 border-2 flex-none w-64 pb-6 hidden md:block">
        <div class="text-gray-700 0 mb-2 mt-3 px-4 flex justify-between">
            <div class="flex-auto">
                <div class="flex items-center mb-6">
                    <svg class="h-2 w-2 fill-current text-green-400 mr-2" viewBox="0 0 20 20"><circle cx="10" cy="10" r="10"></circle></svg>
                    <span class="text-gray-700 opacity-50 text-sm">Adam Wathan</span>
                </div>
            </div>
            <div>
                <svg class="h-6 w-6 fill-current text-gray-700 opacity-25" viewBox="0 0 20 20">
                    <path d="M14 8a4 4 0 1 0-8 0v7h8V8zM8.027 2.332A6.003 6.003 0 0 0 4 8v6l-3 2v1h18v-1l-3-2V8a6.003 6.003 0 0 0-4.027-5.668 2 2 0 1 0-3.945 0zM12 18a2 2 0 1 1-4 0h4z" fill-rule="evenodd" />
                </svg>
            </div>
        </div>
       
        <div class="mb-8">
            <div class="flex items-center mb-3 px-4">
                <svg class="h-2 w-2 fill-current text-green-400  mr-2" viewBox="0 0 20 20"><circle cx="10" cy="10" r="10"></circle></svg>
                <span class="text-gray-700 opacity-75">Adam Wathan <span class="text-grey text-sm">(you)</span></span>
            </div>
            <div class="flex items-center mb-3 px-4">
                <svg class="h-2 w-2 fill-current text-green-400 mr-2" viewBox="0 0 20 20"><circle cx="10" cy="10" r="10"></circle></svg>
                <span class="text-gray-700 opacity-75">David Hemphill</span>
            </div>
            <div class="flex items-center px-4 mb-6 opacity-50">
                <svg class="h-2 w-2 stroke-current text-gray-700 mr-2" viewBox="0 0 22 22"><circle cx="11" cy="11" r="9" fill="none" stroke-width="3"></circle></svg>
                <span class="text-gray-700">Steve Schoger</span>
            </div>
        </div>
        <div>
    
        </div>
    </div>
    <!-- Chat content -->
    <div class="flex-1 flex flex-col bg-white overflow-hidden">
  
        <!-- Chat messages -->
        <div class="px-6 py-4 flex-1 overflow-y-scroll">
            <!-- A message -->
            <div class="flex items-start mb-4 text-sm">
                <img src="https://twitter.com/steveschoger/profile_image" class="w-10 h-10 rounded mr-3">
                <div class="flex-1 overflow-hidden">
                    <div>
                        <span class="font-bold">Steve Schoger</span>
                        <span class="text-grey text-xs">11:46</span>
                    </div>
                    <p class="text-black leading-normal">Hehe, meeting with Manu in a moment. We’ll probably need an hour or so to get this fixed.</p>
                </div>
            </div>
            <!-- A message -->
            <div class="flex items-start mb-4 text-sm">
                <img src="https://twitter.com/adamwathan/profile_image" class="w-10 h-10 rounded mr-3" />
                <div class="flex-1 overflow-hidden">
                    <div>
                        <span class="font-bold">Adam Wathan</span>
                        <span class="text-grey text-xs">12:45</span>
                    </div>
                  <p class="text-black leading-normal">Cool, I’ll let Market know.</p>
                </div>
            </div>
            <hr class="hr-text my-2" :data-content="NewMessage">
            <!-- A message -->
            <div class="flex items-start mb-4 text-sm">
                <img src="https://twitter.com/davidhemphill/profile_image" class="w-10 h-10 rounded mr-3" />
                <div class="flex-1 overflow-hidden">
                    <div>
                        <span class="font-bold">David Hemphill</span>
                        <span class="text-grey text-xs">12:46</span>
                    </div>
                    <p class="text-black leading-normal">Finally done with Manu. Got the fps to be twice as smooth using the smo function instead. All links are now anchored as well.</p>
                </div>
            </div>
            <!-- A message -->
            <div class="flex items-start mb-4 text-sm">
                <img src="https://twitter.com/steveschoger/profile_image" class="w-10 h-10 rounded mr-3">
                <div class="flex-1 overflow-hidden">
                    <div>
                        <span class="font-bold">Steve Schoger</span>
                        <span class="text-grey text-xs">11:46</span>
                    </div>
                    <p class="text-black leading-normal">Done!</p>
                </div>
            </div>
           
            <!-- A message -->
            <div class="flex items-start mb-4 text-sm">
                <img src="https://twitter.com/davidhemphill/profile_image" class="w-10 h-10 rounded mr-3" />
                <div class="flex-1 overflow-hidden">
                    <div>
                        <span class="font-bold">David Hemphill</span>
                        <span class="text-grey text-xs">12:46</span>
                    </div>
                    <p class="text-black leading-normal">Looks awesome, thx! I’ll make sure Ernie pushes this asap. Market will be like.. super-duper happy.</p>
                </div>
            </div>
        </div>
        <div class="pb-6 px-4 flex-none">
            <div class="flex rounded-lg border-2 border-grey overflow-hidden">
                <span class="text-3xl text-grey border-r-2 border-grey p-2">
                    <svg class="fill-current h-6 w-6 block" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M16 10c0 .553-.048 1-.601 1H11v4.399c0 .552-.447.601-1 .601-.553 0-1-.049-1-.601V11H4.601C4.049 11 4 10.553 4 10c0-.553.049-1 .601-1H9V4.601C9 4.048 9.447 4 10 4c.553 0 1 .048 1 .601V9h4.399c.553 0 .601.447.601 1z"/></svg>
                  </span>
                <input type="text" class="w-full my-1 border-0 px-4" placeholder="Message" />
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
data() {
    return {
        NewMessage: 'New Message'
    }
},
}
</script>

<style>

</style>