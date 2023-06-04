import {fetch} from 'wix-fetch';


$w.onReady(function () {
const apiUrl = 'https://api.ambeedata.com/latest/by-lat-lng?lat=47.620422&lng=-122.349358';
const apiKey = '749cadccee798e3ca57bebea6cbe9f785bccca7391ac2f4ba29dc876b6102c75'; // Replace with your actual API key

fetch(apiUrl, {
  method: 'GET',
  headers: {
    'x-api-key': apiKey,
    'Content-type': 'application/json',
  },
})
  .then(response => response.json())
  .then(data => {
    console.log(data);
    
      const aqi = data.stations[0].AQI;
      $w("#hiEl").text = aqi.toString();
          console.log(aqi);

  })

  .catch(error => {
    console.error('Error:', error);
  });

  
});
