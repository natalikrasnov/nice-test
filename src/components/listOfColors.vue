<template>
  <div >
      <div v-for="color in colors" :key="color"> 
          <colorLable :color="color" :onRemove="removeColor.bind()"/>
      </div>
  </div>
</template>

<script>
import colorLable from './colorLable'

export default {
    name: 'ListOfColors',
    components: {
        colorLable
    },
    props: ["searchValue"],
    data () {
        return {
            colors: [
                "Black", "Navy", "DarkBlue", "MediumBlue", "Blue", "DarkGreen", "Green", "Teal", "DarkCyan", "DeepSkyBlue", 
                "DarkTurquoise", "MediumSpringGreen", "Lime", "SpringGreen", "Aqua", "Cyan", "MidnightBlue", "DodgerBlue", "LightSeaGreen", 
                "ForestGreen", "SeaGreen", "DarkSlateGray", "DarkSlateGrey", "LimeGreen", "MediumSeaGreen", "Turquoise", "RoyalBlue", "SteelBlue", 
                "DarkSlateBlue", "MediumTurquoise", "Indigo", "DarkOliveGreen", "CadetBlue", "CornflowerBlue", "RebeccaPurple", "MediumAquaMarine", 
                "DimGray", "DimGrey", "SlateBlue", "OliveDrab", "SlateGray", "SlateGrey", "LightSlateGray", "LightSlateGrey", "MediumSlateBlue", 
                "LawnGreen", "Chartreuse", "Aquamarine", "Maroon", "Purple", "Olive", "Gray", "Grey", "SkyBlue", "LightSkyBlue", "BlueViolet", 
                "DarkRed", "DarkMagenta", "SaddleBrown", "DarkSeaGreen", "LightGreen", "MediumPurple", "DarkViolet", "PaleGreen", "DarkOrchid", 
                "YellowGreen", "Sienna", "Brown", "DarkGray", "DarkGrey", "LightBlue", "GreenYellow", "PaleTurquoise", "LightSteelBlue", "PowderBlue", 
                "FireBrick", "DarkGoldenRod", "MediumOrchid", "RosyBrown", "DarkKhaki", "Silver", "MediumVioletRed", "IndianRed", "Peru", "Chocolate", 
                "Tan", "LightGray", "LightGrey", "Thistle", "Orchid", "GoldenRod", "PaleVioletRed", "Crimson", "Gainsboro", "Plum", "BurlyWood", 
                "LightCyan", "Lavender", "DarkSalmon", "Violet", "PaleGoldenRod", "LightCoral", "Khaki", "AliceBlue", "HoneyDew", "Azure", 
                "SandyBrown", "Wheat", "Beige", "WhiteSmoke", "MintCream", "GhostWhite", "Salmon", "AntiqueWhite", "Linen", "LightGoldenRodYellow", 
                "OldLace", "Red", "Fuchsia", "Magenta", "DeepPink", "OrangeRed", "Tomato", "HotPink", "Coral", "DarkOrange", "LightSalmon", "Orange", 
                "LightPink", "Pink", "Gold", "PeachPuff", "NavajoWhite", "Moccasin", "Bisque", "MistyRose", "BlanchedAlmond", "PapayaWhip", 
                "LavenderBlush", "SeaShell", "Cornsilk", "LemonChiffon", "FloralWhite", "Snow", "Yellow", "LightYellow", "Ivory", "White"
                ]
        }
    },
    methods: {
        removeColor: (color) =>{
            console.log("remove "+color, this)
            //this.colors = this.colors.filter(value=> value !== color)
        }
        
    }
   
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
