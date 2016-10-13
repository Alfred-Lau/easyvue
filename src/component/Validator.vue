<template>
	<validator name="validation">
		<form novalidate>
			<p class="validator-field" v-for="field in fields">
				<label :for="field.id">
					{{field.label}}
				</label>
				<input type="text" :id="field.id" :placeholder="field.placeholder" :field="field.name" v-validate="field.validate">
			</p>
			<pre>
				{{$validation | json}}
			</pre>
		</form>
	</validator>
</template>


<script>
	import Validator from 'vue-validator'

	export default {
		data(){
			return {
				fields:[{
					id:'username',
					label:'username',
					name:'username',
					placeholder:'input your name',
					validate:{
						required:true,
						maxlength:16,
					}
				},{
					id:'message',
					label:'message',
					name:'message',
					placeholder:'input your name',
					validate:{
						required:true,
						maxlength:8,
					}

				}]
			}
		}
	}
</script>