<template>
<div>
  <h4 class="fancy-h4">
    <p>Incredibly important information..</p>
  <slot/> <!-- slot outlet -->
	</h4>
</div>
</template>

<style>
.fancy-h4 {
  color: black;
  background: linear-gradient(315deg, #d38342 25%, #64ff7e);
  border: none;
  padding: 5px 10px;
  margin: 5px;
  border-radius: 8px;

}
</style>