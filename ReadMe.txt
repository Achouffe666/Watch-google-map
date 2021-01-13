Step 1: generate your API key -> https://console.cloud.google.com/projectselector2/google/maps-apis/overview
Step 2: add the script to the html
step 3: add function initmap()
step 4: define map in DOM -> let map = new google.maps.Map(document.querySelector('#map'),options);
step 5: define options in function-> let options = {zoom:12, center: {lat:50.63272972099239,lng:5.585554400943214}}
step 6: define marker +(change marker in beach flag) -> let marker = new google.maps.Marker({
                position:{lat:50.63272972099239,lng:5.585554400943214},
                map:map,
                icon:'https://img.freepik.com/vecteurs-libre/maison-deux-etages_1308-16176.jpg?size=46&ext=jpg'
            }) 
step 7: info Window -> let info = new google.maps.InfoWindow({
    content:'<p>Hello everyone</p>'
})
step 8: addListener to marker -> marker.addListener('click',()=>{
    info.open(map,marker);
})

<!--PIL coordinates: 50.63272972099239, 5.585554400943214 -->
