<template lang="pug">
	v-app(dark)
		v-navigation-drawer(app clipped fixed :mini-variant="mini")

			//- expand icon
			v-list
				v-list-tile(v-if="mini" @click.stop="mini = !mini")
					v-list-tile-action
						v-icon chevron_right
				v-list-tile(avatar tag="div" v-if="!mini")
					v-list-tile-content
						v-list-tile-title Projects
					v-list-tile-action
						v-btn(icon @click.stop="mini = !mini")
							v-icon chevron_left

			//- MENU LIST OF PROJECTS
			v-list
				v-list-tile(avatar)
					v-list-tile-action
						v-btn(fab icon)
							v-avatar(color="teal")
								span.white--text.headline 1
					v-list-tile-content
						v-list-tile-title Project 1
				v-list-tile(avatar)
					v-list-tile-action
						v-btn(fab icon)
							v-avatar(color="purple")
								span.white--text.headline 2
					v-list-tile-content
						v-list-tile-title Project 2
				v-list-tile(avatar)
					v-list-tile-action
						v-btn(fab icon)
							v-avatar(color="indigo")
								span.white--text.headline 3
					v-list-tile-content
						v-list-tile-title Project 3
				v-list-tile(avatar)
					v-list-tile-action
						v-btn(fab icon)
							v-avatar(color="red")
								span.white--text.headline 4
					v-list-tile-content
						v-list-tile-title Project 4
		v-toolbar(app fixed clipped-left)
			v-toolbar-side-icon
			v-toolbar-title Dashboard
			v-spacer
			v-toolbar-items
				v-btn(flat) More
				v-btn(flat) Links
				v-btn(flat) Here
				v-btn(icon)
					v-icon more_vert
		router-view
</template>

<script type="text/javascript">
	export default {
		data: () => ({
			mini: true
		})
	}
</script>

<style lang="scss">

</style>
