<template>
	<ripper>
		<template slot="title">
			<slot name="title" class="title">
				<i v-if="icon" :class="[icon, 'icon']"></i>
				{{title}}
			</slot>
		</template>
		<slot />
	</ripper>
</template>

<script lang="ts">
import * as Vue from 'vue'
import {Component, Inject, Model, Prop, Watch, Emit} from 'vue-property-decorator'
import {Ripper} from 'vue-ripper'

@Component({components:{Ripper}})
export default class Tab extends Vue {
	@Prop() icon: string
	@Prop() title: string
	@Prop() name: string
}
</script>