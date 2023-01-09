<template>
  <div class="search">

    <div class="search__container">
      <h1 class="search__title">Advanced search</h1>
      <div class="search__filter">
          <h3 class="search__filter_title">Acapellas</h3>
          <h3 class="search__filter_title">Loops & Samples</h3>
          <h3 class="search__filter_title">MIDI</h3>
          <h3 class="search__filter_title">Presets</h3>
          <h3 class="search__filter_title">Projects</h3>
          <h3 class="search__filter_title">VST</h3>
      </div>


    <div class="search__filter_line"></div>
    <div class="selection_wrapper">
    <Selection
      v-for="selection in selection_list"
      :key="`selection-${selection.id}`"
      :title="selection.title"
      :subtitle="selection.subtitle"
      />
    </div>
  </div>
  </div>

</template>

<script>
import "@/assets/css/search.scss"

export default{
  data: () => ({
    selection_list: [
      {
        id: 1,
        title: 'Genre',
        subtitle: 'GARAGE / BASSLINE / GRIME'
      },
      {
        id: 2,
        title: 'License',
        subtitle: 'Commercial license required'
      },
      {
        id: 3,
        title: 'Type',
        subtitle: 'Choose type'
      },
      {
        id: 4,
        title: 'Tags',
        subtitle: 'Choose tag'
      },

    ]
  }),

  components: {
    Selection: () => import('@/components/controls/selection.vue')
  }
}
</script>
