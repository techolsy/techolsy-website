<script>
  import { writable } from 'svelte/store';
  import { SvelteFlow, Background, Controls, Handle } from '@xyflow/svelte';
  import '@xyflow/svelte/dist/style.css';
  import CustomNode from './CustomNode.svelte';

  const nodes = writable([
    {
      id: '1', 
      position: { x: 320, y: 50 },
      type: 'customNode',
      data: { label: 'netgate SG-1100' },
    },
    {
      id: '2',
      position: { x: 350, y: 150},
      type: 'customNode',
      data: { label: 'MokerLink' },
    },
    {
      id: '3',
      position: { x: 650, y: 300},
      type: 'customNode',
      data: { label: 'UniFi AC Lite'}
    },
    {
      id: '4',
      position: { x: 450, y: 300},
      type: 'customNode',
      data: { label: 'PVE01'}
    },
    {
      id: '5',
      position: { x: 250, y: 300},
      type: 'customNode',
      data: { label: 'PVE02'}
    },
    {
      id: '6',
      position: { x: 50, y: 300},
      type: 'customNode',
      data: { label: 'PBS'}
    },
  ]);

  const edges = writable([
    { 
      id: '1-2', 
      source: '1', 
      target: '2',
    },
    { 
      id: '2-3', 
      source: '2', 
      target: '3',
    },
    { 
      id: '2-4', 
      source: '2', 
      target: '4',
    },
    { 
      id: '2-5', 
      source: '2', 
      target: '5',
    },
    { 
      id: '2-6', 
      source: '2', 
      target: '6',
    },
  ]);

  const nodeTypes = {
    customNode: CustomNode
  };
</script>

<h3>Networking</h3>
<p>
  I have a very simple networking setup, it consists of one gateway, one switch and one access point.
  as for the gateway is a <i>netgate SG 1100</i> running pfSense, the switch is a <i>MokerLink 2G080110GSM</i> 
  and the access point is a <i>UniFi AP Lite</i>.
</p>
<p>
  The gateway is connected to my ISP and I have created an extra vlan that I am using for IOT devices. 
  The switch is not doing much extra more than tagging along the extra vlan to my AP and having my wired pc's connected.
  All my wireless devices are connected to my AP, and it serves both my networks I have created. 
  Below is a simple diagram showing the topology of how everything is connected.
</p>

<details>
  <summary>Network Diagram</summary>
  <div class="diagram">
    <SvelteFlow {nodes} {edges} {nodeTypes} fitView>
      <Background bgColor="rgba(32,38,50,1)" patternColor="rgba(1,170,255,0.5)" />
      <Controls />
    </SvelteFlow>
  </div>
</details>

<style>
  .diagram {
    height: 50vh;
  }
</style>
