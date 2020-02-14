<script>
  import Tailwindcss from "./Tailwindcss.svelte";
  import LineChart from "./components/LineChart.svelte";
  import MapTest from "./components/MapTest.svelte";
</script>

<style>
  .chart-container {
    height: 100%;
    width: 100%;
  }
</style>

<Tailwindcss />

<div class="container mx-auto p-3">
  <h1 class="title">Title</h1>
  <h2 class="subtitle">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsam eos, eaque
    suscipit autem dolores ipsum qui a expedita nesciunt cum ducimus aperiam
    rerum sequi et, incidunt placeat repudiandae totam amet!
  </h2>
</div>
<div class="h-20" />
<div class="container mx-auto">
  <div class="flex flex-wrap mx-auto">
    <div class="w-full md:w-1/3 p-3">
      <h2>Transmissions over time</h2>
      <h3>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus
        numquam eveniet necessitatibus quidem mollitia dolorum deserunt et
        dolore fugit quas voluptas, quis sapiente ab, placeat doloribus
        perferendis sunt sed eum.
      </h3>
    </div>
    <div class="w-full md:w-2/3 h-64 p-3">
      <div class="chart-container">
        <LineChart />
      </div>
    </div>
  </div>
</div>
<div class="h-20" />
<div class="container mx-auto">
  <div class="flex flex-wrap mx-auto">
    <div class="w-full md:w-2/3 h-64 p-3">
      <div class="chart-container">
        <MapTest />
      </div>
    </div>
    <div class="w-full md:w-1/3 p-3">
      <h2>Packets in space</h2>
      <h3>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus
        numquam eveniet necessitatibus quidem mollitia dolorum deserunt et
        dolore fugit quas voluptas, quis sapiente ab, placeat doloribus
        perferendis sunt sed eum.
      </h3>
    </div>
  </div>
</div>
