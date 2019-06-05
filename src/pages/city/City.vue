<template>
	<div>
		<city-header></city-header>
    <city-search :citys="citys"></city-search>
    <city-list :citys="citys" :hot="hotCitys" :letter="letter"></city-list>
    <city-alphabet :citys="citys" @change = "handleLetterChange"></city-alphabet>
	</div>
</template>
<script>
import axios from 'axios'
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data  () {
    return {
      citys: {},
      hotCitys: [],
      letter: ''
    }
  },
  methods: {
    getCityInfo () {
      axios.get('./api/city.json')
        .then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.citys = data.citys
        this.hotCitys = data.hotCitys
      }
    },
    handleLetterChange (letter) {
      this.letter = letter
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>
<style lang="stylus" scoped>
</style>
