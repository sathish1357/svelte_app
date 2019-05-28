<link href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.3.1/css/bootstrap.min.css" rel="stylesheet">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/css/bootstrap.min.css"> 
<script>
	import {settings}  from "./SettingsStore.js";
</script>

<div class="mx-auto" style="width: 500px;">
<h1>	
  HTML Form Code Generation
</h1>
<hr>
<div class="input-group">		
	<span class="input-group-addon">Select Input Type</span>
	<select class="form-control" bind:value={$settings.HtmlInputs.type}>
		<option selected></option>
		<option value="button">Button</option>
    <option value="checkbox">CheckBox</option>
    <option value="color">Color</option>
    <option value="date">Date</option>
    <option value="datetime-local">DateTime-Local</option>
    <option value="email">Email</option>
    <option value="file">File</option>
    <option value="hidden">Hidden</option>
    <option value="image">Image</option>
    <option value="month">Month</option>
    <option value="number">Number</option>
    <option value="password">Password</option>
    <option value="radio">Radio</option>
    <option value="range">Range</option>
    <option value="reset">Reset</option>
    <option value="select">Select</option>
    <option value="search">Search</option>
    <option value="submit">Submit</option>
    <option value="tel">Tel</option>
    <option value="text">Text</option>
    <option value="textarea">TextArea</option>
    <option value="time">Time</option>
    <option value="url">Url</option>
    <option value="week">Week</option>
		</select>
	</div>
  <br>
 <div class="input-group">
    <span class="input-group-addon">Label</span>
    <input type="text" class="form-control" bind:value={$settings.HtmlInputs.label} placeholder="Enter Label Of Input">
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">ID</span>
    <input type="text" class="form-control" bind:value={$settings.HtmlInputs.id} placeholder="Enter id Of Input">
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">Name</span>
    <input type="text" class="form-control" bind:value={$settings.HtmlInputs.name} placeholder="Enter Name Of Input">
  </div>
<br>

{#if $settings.HtmlInputs.type == "textarea"}
<div class="input-group">
    <span class="input-group-addon">Rows</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.rows} placeholder="Enter number of Rows of TextArea">
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">Columns</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.cols} placeholder="Enter nubmer of columns of TextArea">
  </div>
<br>
{/if}

{#if $settings.HtmlInputs.type == "radio" || $settings.HtmlInputs.type == "checkbox"}
<div class="input-group">
    <span class="input-group-addon">isChecked</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.checked}>
		<option selected></option>
		<option value="Yes">Yes</option>
		<option value="No">No</option>
	</select>
  </div>
<br>
{/if}
<div class="input-group">
    <span class="input-group-addon">isRequired</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.required}>
		<option selected></option>
		<option value="Yes">Yes</option>
		<option value="No">No</option>
	</select>
  </div>
<br>
{#if $settings.HtmlInputs.type == "radio" || $settings.HtmlInputs.type == "checkbox" || $settings.HtmlInputs.type == "range" || $settings.HtmlInputs.type == "text" || $settings.HtmlInputs.type == "hidden" || $settings.HtmlInputs.type == "email" || $settings.HtmlInputs.type == "password" || $settings.HtmlInputs.type == "search"|| $settings.HtmlInputs.type == "url"|| $settings.HtmlInputs.type == "submit" || $settings.HtmlInputs.type == "reset" || $settings.HtmlInputs.type == "number" || $settings.HtmlInputs.type == "button"
}
<div class="input-group">
    <span class="input-group-addon">Value</span>
    <input type="text" class="form-control" bind:value={$settings.HtmlInputs.value} placeholder="Enter Value for Input">
  </div>
<br>
{/if}
{#if $settings.HtmlInputs.type == "text" || $settings.HtmlInputs.type == "email" || $settings.HtmlInputs.type == "password" || $settings.HtmlInputs.type == "search"|| $settings.HtmlInputs.type == "url"
}
<div class="input-group">
    <span class="input-group-addon">MaxLength</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.maxlength} placeholder="Enter MaxLength of Input">
  </div>
<br>

<div class="input-group">
    <span class="input-group-addon">MinLength</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.minlength} placeholder="Enter MinLength of Input">
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">Size</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.size} placeholder="Enter size of Input">
  </div>
<br>
{/if}
{#if $settings.HtmlInputs.type == "range" || $settings.HtmlInputs.type == "number" || $settings.HtmlInputs.type == "time" || $settings.HtmlInputs.type == "date"}
<div class="input-group">
    <span class="input-group-addon">MaxValue</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.max} placeholder="Enter MaxValue of Input">
  </div>
<br>

<div class="input-group">
    <span class="input-group-addon">MinValue</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.min} placeholder="Enter MinValue of Input">
  </div>
<br>
{/if}
{#if $settings.HtmlInputs.type == "range" || $settings.HtmlInputs.type == "number"}
<div class="input-group">
    <span class="input-group-addon">StepValue</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.step} placeholder="Enter StepValue of Input">
  </div>
<br>
{/if}
{#if $settings.HtmlInputs.type == "image"}
<div class="input-group">
    <span class="input-group-addon">Height</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.height} placeholder="Enter Height of Input">
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">Width</span>
    <input type="number" class="form-control" bind:value={$settings.HtmlInputs.width} placeholder="Enter Width of Input">
  </div>
<br>
{/if}
{#if ($settings.HtmlInputs.type != "button" && $settings.HtmlInputs.type != "reset" && $settings.HtmlInputs.type !="submit" ) && ($settings.HtmlInputs.type == "text" || $settings.HtmlInputs.type == "email" || $settings.HtmlInputs.type == "password" || $settings.HtmlInputs.type == "search"|| $settings.HtmlInputs.type == "url" || $settings.HtmlInputs.type == "number")
}
<div class="input-group">
    <span class="input-group-addon">Choose Pattern</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.pattern}>
		<option selected></option>
		<option value="[A-Za-z]{'{3}'}">"Three letter country code"</option>
    <option value="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{'{8,}'}">"Must contain at least one number and one uppercase and lowercase letter, and at least 8 or more characters"</option>
		<option value="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{'{2,}'}$">email must be in the following order: characters@characters.domain (characters followed by an @ sign, followed by more characters, and then a "."</option>
    <option value="customize">Customize</option>
	</select>
  <br>
</div>

  <br>
  {#if $settings.HtmlInputs.pattern == "customize"}
  <div class="input-group">
    <span class="input-group-addon">Own Pattern</span>
    <input type="text" class="form-control" bind:value={$settings.HtmlInputs.own_pattern} placeholder="Enter Pattern Of Input">
  </div>  
  {/if}
  <br>
<div class="input-group">
    <span class="input-group-addon">isReadOnly</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.readonly}>
		<option selected></option>
		<option value="Yes">Yes</option>
		<option value="No">No</option>
	</select>
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">isDisabled</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.disabled}>
		<option selected></option>
		<option value="Yes">Yes</option>
		<option value="No">No</option>
	</select>
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">isAutoFocus</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.autofocus}>
		<option selected></option>
		<option value="Yes">Yes</option>
		<option value="No">No</option>
	</select>
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">isAutoComplete</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.autocomplete}>
		<option selected></option>
		<option value="Yes">Yes</option>
		<option value="No">No</option>
	</select>
  </div>
<br>
<div class="input-group">
    <span class="input-group-addon">PlaceHolder</span>
    <input type="text" class="form-control" bind:value={$settings.HtmlInputs.placeholder} placeholder="Enter PlaceHolder For Input">
  </div>
<br>
{/if}
<div class="input-group">
    <span class="input-group-addon">Choose Formenctype</span>
   <select class="form-control" bind:value={$settings.HtmlInputs.autocomplete}>
		<option selected></option>
		<option value="application/x-www-form-urlencoded">All characters will be encoded before sent</option>
    <option value="multipart/form-data">multipart/form-data is(use this when you are using forms that have a file upload control)</option>
		<option value="text/plain">text/plain (Spaces are converted to "+" symbols, but no characters are encoded)</option>
	</select>
  </div>
<br>
<hr>
</div>