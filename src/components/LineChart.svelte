<script>
  import { LayerCake, Svg } from "layercake";
  import points from "../data/points.csv";
  import Line from "../chart-components/Line.svelte";
  import Area from "../chart-components/Area.svelte";
  import AxisX from "../chart-components/AxisX.svelte";
  import AxisY from "../chart-components/AxisY.svelte";

  points.forEach(row => {
    row.myY = +row.myY;
  });
</script>

<LayerCake
  padding={{ right: 10, bottom: 20, left: 25 }}
  x={'myX'}
  y={d => d.myY}
  yDomain={[0, null]}
  data={points}>
  <Svg>
    <AxisX />
    <AxisY />
    <Line />
    <Area />
  </Svg>
</LayerCake>
