<template>



  <div class="md:w-10/12 w-screen p-3 mb-4 font-medium">
  
  <div class="flex justify-between md:hidden block">
    <div>
        <form class="mb-4 md:mb-0 md:w-1/4">
    <label class="hidden" for="search-form">Search</label>
    <input class=" p-2 rounded-0 w-full" placeholder="Search" type="text">
    <!-- <button class="hidden">Submit</button> -->
  </form>
    </div>
<div>
  <i class="fa fa-lg mt-3 text-gray-500 fa-calendar px-2"></i>
  <i class="fa fa-bell mt-3 fa-lg text-gray-500"></i>
</div>
  </div>
    <div class="h-auto flex-none bg-white rounded-t lg:rounded-t-none lg:rounded-l text-center shadow-lg ">
      <div class=" rounded-t overflow-hidden">
        <div class="flex justify-between text-lg header-background text-gray-900 py-3">
          <h6 class="pl-2 text-left font-semibold	">This Month</h6>
          <div>
                <span class=" text-right pr-4">
            <select class="appearance-none">
              <option>Sales</option>

            </select>
          </span>
          </div>
        </div>
        <div class="p-3">
          <bar-chart :data="barChartData" :options="barChartOptions" :height="ht" />
        </div>
      </div>
    </div>
    <div class="flex flex-col md:flex-row my-3 rounded-t">
      <div class="flex-auto mx-2 rounded-t  lg:rounded-t-none lg:rounded-l shadow-lg">
        <div class=" flex justify-between text-lg header-background text-gray-900 py-3">
          <h6 class="pl-2 text-left font-semibold	">Tasks</h6>
         <div>
            <span class="text-right pr-4">
            <select class="appearance-none mx-2">
              <option>Sort</option>

            </select>
            <i class="fa fa-lg p-2 bg-gray-300 text-gray-50 rounded-0 fa-plus-square"></i>
             </span>
         </div>
         
        </div>
        <div class="space-y-0">
          <div class="block border-b py-3 border-gray-300">
            <div class="flex justify-between">
              <div class=" text-left px-2 font-semibold"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-300 rounded-0 fa-plus-square"></i> Send prototype to team
              </div>
              <div class="text-right text-gray-500 mx-3">Today <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-indigo-900 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
          <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-300 rounded-0 fa-plus-square"></i> Review content with
                copywriter</div>
              <div class="text-right text-gray-500 mx-3">Yesterday <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
          <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-300 rounded-0 fa-plus-square"></i> Optimize hero images
              </div>
              <div class="text-right text-gray-500 mx-3">16 July <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
               <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-300 rounded-0 fa-plus-square"></i> Add loading screen after sign up
              </div>
              <div class="text-right text-gray-500 mx-3">14 July <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-indigo-900 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
                <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold line-through"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-500 rounded-0 fa-check"></i> Get file structure ready for cms
              </div>
              <div class="text-right text-gray-500 mx-3">28 June <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
                <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold line-through"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-500 rounded-0 fa-check"></i> Update style guide with new colors
              </div>
              <div class="text-right text-gray-500 mx-3">25 June <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
                <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold line-through"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-500 rounded-0 fa-check"></i> Define grid for editor
              </div>
              <div class="text-right text-gray-500 mx-3">24 June <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
                <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold line-through"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-500 rounded-0 fa-check"></i> Fix footer on mobile
              </div>
              <div class="text-right text-gray-500 mx-3">21 June <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
               <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2 font-semibold line-through"><i
                  class="fa fa-lg p-2 bg-gray-300 text-gray-500 rounded-0 fa-check"></i> Mobile navigation not working in ie
              </div>
              <div class="text-right text-gray-500 mx-3">21 June <i
                  class="fa font-semibold text-gray-500 ml-10 fa-lg fa-paperclip"></i> <i
                  class="fa fa-lg ml-5 p-2 bg-gray-400 text-white rounded-sm fa-star"></i></div>
            </div>
          </div>
        </div>
      </div>
      <div class="md:flex-1 rounded-t  lg:rounded-t-none lg:rounded-l shadow-lg">
         <div class=" grid grid-cols-3 gap-4 text-lg header-background text-gray-900 py-3">
          <h6 class="pl-2 text-left col-span-2 font-semibold">Projects</h6>
          <span class="text-right pr-4">
            <i class="fa p-2 text-indigo-500 rounded-0 fa-plus"></i>
          </span>
        </div>
        <div class="space-y-0">
          <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              
              <div class="col-start-1 col-end-1 text-left px-2">Flowychart Editor
                <p class="text-gray-500">Enigm</p>
              </div>
              <div class="text-right mx-3"> <div class=" md:flex  xl:flex px-4 items-center">
              <div class="h-1 rounded-full flex-grow my-3" style="background: orange;"></div>
            </div></div>
            </div>
          </div>
           <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2">Landing Page
                <p class="text-gray-500">Giddify</p>
              </div>
                <div class="text-right mx-3"> <div class=" md:flex  xl:flex px-4 items-center">
              <div class="h-1 rounded-full flex-grow my-3" style="background: red;"></div>
            </div></div>
            </div>
          </div>
           <div class="block border-b py-3 border-gray-300">
            <div class="grid grid-cols-2">
              <div class="col-start-1 col-end-1 text-left px-2">Strand App
                <p class="text-gray-500">Mondemi</p>
              </div>
               <div class="text-right mx-3"> <div class=" md:flex  xl:flex px-4 items-center">
              <div class="h-1 rounded-full flex-grow my-3" style="background: green;"></div>
            </div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
       <!-- <NuxtLink to="/chat">
      <Button class=" bg-indigo-500 m-2 shadow rounded-lg text-white p-2">Route to Chat View Page</Button>
    </NuxtLink> -->
  </div>

</template>

<script>
  import BarChart from '~/components/BarChart'
  export default {
    components: {
      BarChart
    },
    data() {
      return {
        ht: 164,
        barChartData: {
          labels: [
            'Jan',
            'Feb',
            'Mar',
            'Apr',
            'May',
            'Jun',
            'Jul',
            'Aug',
            'Sep',
            'Oct',
            'Nov', 'Dec'
          ],
          datasets: [{
            label: 'Months',
            data: [10, 5, 15, 20, 25, 18, 35, 32, 34, 45, 30, 20],
            backgroundColor: '#575BDE'
          }, ]
        },
        barChartOptions: {
          responsive: true,
          legend: {
            display: false
          },
          title: {
            display: false,
            fontSize: 24,
            fontColor: '#6b7280'
          },
          tooltips: {
            backgroundColor: '#17BF62'
          },
          scales: {
            xAxes: [{
              gridLines: {
                display: false
              }
            }],
            yAxes: [{
              ticks: {
                beginAtZero: true
              },
              gridLines: {
                display: true
              }
            }]
          }
        }
      }
    }

  }

</script>

<style>
  * {
    font-family: 'Lato', sans-serif;
  }

  .dashboard-heading {
    font-family: 'Lato', sans-serif;
    font-style: normal;
    font-size: 16px;
    line-height: 32px;
  }

</style>
