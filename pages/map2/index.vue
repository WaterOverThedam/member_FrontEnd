<template>
       <div>
         <div id="map" style="display:none"></div>
         <div class="button-group">
             <input type="button" class="button" value="显示当前城市"      onClick="javascript:showCityInfo()"/>     
         </div>
         <div id="tip"></div>
       </div>
  </template>

  <style>
    .amap-demo {
      height: 300px;
    }
  </style>

  <script>

    module.exports = {
      head:{
        title:"member",
        script: [
            {src: 'https://webapi.amap.com/maps?v=1.4.6&key=905cd6594c65b6cb1af4b6f21ff40946&plugin=AMap.CitySearch'},
            {src: 'js/map.js'}
        ]
      },
      data: function() {
        let self = this;
      }
    
    };
</script>