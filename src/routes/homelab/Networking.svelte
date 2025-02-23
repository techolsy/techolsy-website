<script>
  import { writable } from 'svelte/store';
  import { SvelteFlow, Background, Controls, Handle } from '@xyflow/svelte';
  import '@xyflow/svelte/dist/style.css';

  import CustomNode from '$lib/components/CustomNode.svelte';
  import Accordion from '$lib/components/Accordion.svelte';

  const pTags = "text-xl py-1";

  const nodes = writable([
    {
      id: '1', 
      position: { x: 350, y: 50 },
      data: { label: 'netgate SG-1100' },
    },
    {
      id: '2',
      position: { x: 350, y: 150},
      data: { label: 'MokerLink' },
    },
    {
      id: '3',
      position: { x: 650, y: 300},
      data: { label: 'UniFi AC Lite'}
    },
    {
      id: '4',
      position: { x: 450, y: 300},
      data: { label: 'PVE01'}
    },
    {
      id: '5',
      position: { x: 250, y: 300},
      data: { label: 'PVE02'}
    },
    {
      id: '6',
      position: { x: 50, y: 300},
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

<h3 class="text-3xl">Networking</h3>

<p class="{ pTags }">
  I have a very simple networking setup, it consists of one gateway, one switch and one access point.
  as for the gateway is a <i>netgate SG 1100</i> running pfSense, the switch is a <i>MokerLink 2G080110GSM</i> 
  and the access point is a <i>UniFi AP Lite</i>.
</p>

<p class="{ pTags }">
  The gateway is connected to my ISP and I have created an extra vlan that I am using for IOT devices. 
  The switch is not doing much extra more than tagging along the extra vlan to my AP and having my wired pc's connected.
  All my wireless devices are connected to my AP, and it serves both my networks I have created. 
  Below is a simple diagram showing the topology of how everything is connected.
</p>

<div class="py-3">
  <Accordion title="Network Diagram">
    <div class="h-[400px]">
      <SvelteFlow {nodes} {edges} fitView />
    </div>
  </Accordion>
</div>
