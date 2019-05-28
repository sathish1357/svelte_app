<link href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.3.1/css/bootstrap.min.css" rel="stylesheet">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/css/bootstrap.min.css"> 
<script>
	import {settings}  from "./SettingsStore.js";
</script>
<div class="mx-auto" style="width: 500px;">

	<h2 class="mt-3 mb-3 col">AngularJS Code Generator</h2>
	
	<br/>
	<div class="input-group">
    	<span class="input-group-addon"><b>FormName</b></span>
	    <input type="text" class="form-control" bind:value={$settings.form_name} placeholder="Enter Name Of Form">
  	</div>	
	<br>
	<div class="input-group">
    	<span class="input-group-addon"><b>ng-model</b></span>
	    <input type="text" class="form-control" bind:value={$settings.angularJs.ng_model} placeholder="Enter ng_model Of Input">
  	</div>	
	<br>
	
	<div class="input-group">
    	<span class="input-group-addon">ng-required</span>
   		<select class="form-control" bind:value={$settings.angularJs.required}>
			<option selected></option>
			<option value="YES">true - Mandatory field</option>
			<option value="NO">false - Optional field - DUMMY</option>
		</select>		
	</div>	
	<br/>
	
<div class="input-group">
    <span class="input-group-addon">Choose Pattern</span>
   <select class="form-control" bind:value={$settings.angularJs.ng_pattern}>
		<option selected></option>
		<option value="[A-Za-z]{'{3}'}">"Three letter country code"</option>
    <option value="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{'{8,}'}">"Password ->Must contain at least one number and one uppercase and lowercase letter, and at least 8 or more characters"</option>
		<option value="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{'{2,}'}$">email -> must be in the following order: characters@characters.domain (characters followed by an @ sign, followed by more characters, and then a "."</option>
    <option value="customize">Customize</option>
	</select>
  <br>
</div>

  <br>
  {#if $settings.angularJs.ng_pattern == "customize"}
  <div class="input-group">
    <span class="input-group-addon">Own Pattern</span>
    <input type="text" class="form-control" bind:value={$settings.angularJs.own_ng_pattern} placeholder="Enter Pattern Of Input">
  </div>  
  {/if}
  <br>

	<div class="input-group">
    	<span class="input-group-addon">ng-maxlength</span>
    	<input type="number" class="form-control" bind:value="{$settings.angularJs.ng_maxlength}" placeholder="Enter ng-MaxLength of Input">
		<div class="input-group-prepend">
			<span class="input-group-text" on:click="{ e => $settings.angularJs.ng_maxlength = null}">X</span>
		</div>
  	</div>  	
	<br>
	<div class="input-group">
		<span class="input-group-addon">ng-minLength</span>
		<input type="number" class="form-control" bind:value="{$settings.angularJs.ng_minlength}" placeholder="Enter ng-MinLength of Input">
		<div class="input-group-prepend">
				<span class="input-group-text" on:click="{ e => $settings.angularJs.ng_minlength = null}">X</span>
		</div>
	</div>
	<br>


	<div class="input-group">
    	<span class="input-group-addon">ng-maxValue</span>
    	<input type="number" class="form-control" bind:value="{$settings.angularJs.ng_max}" placeholder="Enter ng-MaxValue of Input">
		<div class="input-group-prepend">
			<span class="input-group-text" on:click="{ e => $settings.angularJs.ng_max = null}">X</span>
		</div>
  	</div>  	
	<br>
	<div class="input-group">
		<span class="input-group-addon">ng-minValue</span>
		<input type="number" class="form-control" bind:value="{$settings.angularJs.ng_min}" placeholder="Enter ng-MinValue of Input">
		<div class="input-group-prepend">
				<span class="input-group-text" on:click="{ e => $settings.angularJs.ng_min = null}">X</span>
		</div>
	</div>
	<br>
	
	<div class="input-group">
    	<span class="input-group-addon">ng-disabled</span>
   		<select class="form-control" bind:value={$settings.angularJs.ng_disabled}>
			<option selected></option>
			<option value="YES">true - Accessable field</option>
			<option value="NO">false - not Accessable field - DUMMY</option>
		</select>
		<div class="input-group-prepend">
			<span class="input-group-text" on:click="{ e => $settings.angularJs.ng_disabled = ""}">X</span>
		</div>
	</div>	
	<br/>
</div>
<br/><br/><br/><br/><br/>