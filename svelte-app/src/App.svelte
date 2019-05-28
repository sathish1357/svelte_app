
<link href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.3.1/css/bootstrap.min.css" rel="stylesheet">
<script>		
	import {settings}  from "./SettingsStore.js";	
	import HTMLAttributes from "./HTMLAttributes.svelte";
	import AngularJs_1_x from "./AngularJs_1_x.svelte";
	
</script>

<h3 style="color:green">
	Your code is Below	
</h3>
<pre class="border">
&lt;label {#if $settings.HtmlInputs.id} for="{$settings.HtmlInputs.id}" {/if}&gt;{$settings.HtmlInputs.label}:&lt;/label&gt;
</pre>
<br>
<pre class="border hidden">
{#if $settings.HtmlInputs.type == "textarea"}
	&lt;textarea rows="{$settings.HtmlInputs.rows}" cols="{$settings.HtmlInputs.cols}"  	
{:else}
	&lt;input type="{$settings.HtmlInputs.type}" {/if}

	{#if $settings.HtmlInputs.name}name="{$settings.HtmlInputs.name}" {/if} 
	{#if $settings.HtmlInputs.value}value="{$settings.HtmlInputs.value}" {/if} 
	{#if $settings.HtmlInputs.id}id="{$settings.HtmlInputs.id}"{/if} 
	{#if $settings.HtmlInputs.autofocus == "Yes"} autofocus {/if} 
	{#if $settings.HtmlInputs.required=="Yes"}required{/if} 
	{#if $settings.HtmlInputs.pattern || $settings.HtmlInputs.own_pattern}
		{#if $settings.HtmlInputs.pattern != "customize"} pattern="{$settings.HtmlInputs.pattern}"  {:else} pattern="{$settings.HtmlInputs.own_pattern}"{/if} 
	{/if}
	{#if $settings.HtmlInputs.checked=="Yes"}checked{/if} 
	{#if $settings.HtmlInputs.autocomplete=="Yes"} autocomplete="on"  {:else if $settings.HtmlInputs.autocomplete=="No" }autocomplete="off"{/if} 
	{#if $settings.HtmlInputs.placeholder} placeholder="{$settings.HtmlInputs.placeholder}"{/if}
	{#if $settings.HtmlInputs.size} size="{$settings.HtmlInputs.size}" {/if}
	{#if $settings.HtmlInputs.maxlength } maxlength ="{$settings.HtmlInputs.maxlength }" {/if}
	{#if $settings.HtmlInputs.minlength } minlength ="{$settings.HtmlInputs.minlength }" {/if}                    
	{#if $settings.HtmlInputs.formenctype=="application/x-www-form-urlencoded"} formenctype="application/x-www-form-urlencoded"  {:else if $settings.HtmlInputs.formenctype =="multipart/form-data" }formenctype="multipart/form-data" {:else if $settings.HtmlInputs.formenctype =="text/plain" }formenctype="text/plain"{/if} 		
	{#if $settings.HtmlInputs.step } step ="{$settings.HtmlInputs.step }" {/if}        
	{#if $settings.HtmlInputs.min} min ="{$settings.HtmlInputs.min }" {/if}        
	{#if $settings.HtmlInputs.max } max ="{$settings.HtmlInputs.max }" {/if}        
	{#if $settings.HtmlInputs.width } width ="{$settings.HtmlInputs.width }" {/if}
	{#if $settings.HtmlInputs.height } height ="{$settings.HtmlInputs.height }" {/if}                                   
	{#if $settings.HtmlInputs.readonly=="Yes"}readonly{/if} 
	{#if $settings.HtmlInputs.disabled=="Yes"}disabled{/if} 
	&gt; 
	
	{#if $settings.HtmlInputs.type == "textarea"}&lt;/textarea&gt;{/if}
	&lt;br/&gt;

</pre>
<hr>
<h1>AngularJs_1_x code</h1>
<pre>
	&lt;label {#if $settings.HtmlInputs.id} for="{$settings.HtmlInputs.id}" {/if}&gt;{$settings.HtmlInputs.label}:&lt;/label&gt;
	&lt;input type="{$settings.HtmlInputs.type}" 			
		{#if $settings.HtmlInputs.name}name="{$settings.HtmlInputs.name}"{/if}
		{#if $settings.HtmlInputs.id}id="{$settings.HtmlInputs.id}"{/if}
		{#if $settings.HtmlInputs.autocomplete === "OFF"}autocomplete="off"{/if}
		{#if $settings.angularJs.ng_model}ng-model="{$settings.angularJs.ng_model}"{/if}
		{#if $settings.angularJs.ng_required === "YES"}ng-required="true"{/if}
		{#if $settings.angularJs.ng_pattern || $settings.angularJs.own_ng_pattern }
			{#if $settings.angularJs.ng_pattern !="customize"}ng-pattern="{$settings.angularJs.ng_pattern}" {:else} ng-pattern="{$settings.angularJs.own_ng_pattern}"{/if} 
		{/if}
		{#if $settings.angularJs.ng_maxlength}ng-maxlength="{$settings.angularJs.ng_maxlength}"{/if}
		{#if $settings.angularJs.ng_minlength }ng-minlength="{$settings.angularJs.ng_minlength}"{/if}
		{#if $settings.angularJs.ng_max }ng-max="{$settings.angularJs.ng_max}"{/if}
		{#if $settings.angularJs.ng_min }ng-min="{$settings.angularJs.ng_min}"{/if}
		{#if $settings.angularJs.ng_disabled === "YES"}ng_disabled="true"{/if}
		/&gt;

																				
	{#if $settings.HtmlInputs.type == "email" }&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.{$settings.HtmlInputs.type}" &gt; enter valid {$settings.HtmlInputs.type} .&lt/span&gt; &lt;br/&gt;{/if}
	{#if $settings.angularJs.ng_required === "YES"}&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.required" &gt; {$settings.HtmlInputs.name}  is required.&lt/span&gt; &lt;br/&gt;{/if}
	{#if $settings.angularJs.ng_pattern || $settings.angularJs.own_ng_pattern }&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.pattern"&gt; {$settings.HtmlInputs.name}  Should match the pattern.&lt/span&gt; &lt;br/&gt;{/if}
	{#if $settings.angularJs.ng_maxlength }&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.maxlength" &gt; maxlength is {$settings.angularJs.ng_maxlength}. &lt/span&gt; &lt;br/&gt;{/if}
	{#if $settings.angularJs.ng_minlength }&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.maxlength" &gt; minlength is {$settings.angularJs.ng_maxlength}.&lt/span&gt; &lt;br/&gt;{/if}
	{#if $settings.angularJs.ng_max }&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.max" &gt; maxvalue is {$settings.angularJs.ng_max}.&lt/span&gt; &lt;br/&gt;{/if}
	{#if $settings.angularJs.ng_min }&lt;span style="color:red" ng-show="{$settings.form_name}.{$settings.HtmlInputs.name}.$touched && {$settings.form_name}.{$settings.HtmlInputs.name}.$error.min" &gt; minvalue is {$settings.angularJs.ng_min}.&lt/span&gt; &lt;br/&gt;{/if}

	 

</pre>

<HTMLAttributes />
<AngularJs_1_x />