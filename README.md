# Implement Google Maps in Lightning Components


<a href="https://githubsfdeploy.herokuapp.com?owner=sthornley&repo=Blog-GoogleMaps-Contact-Sample">
  <img alt="Deploy to Salesforce" src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/deploy.png">
</a>
<br/><br/>

GogoleMaps.vfp: Visualforce Page
- Google Maps library
- Listen to “message” event for window.postMessage
- Send “message” event to Lightning Component

GoogleMaps.cls: Apex Class
- Return list of all accounts with BillingLongitude and Billing Latotude

GoogleMaps.cmp: Lightning Component
- Accept data to draw on Google Map
- Listen to “message” event for window.postMessage
- Send data to iFramed Visualforce after iFrame has loded successfully

GooleMapsContainer.cmp: Lightning Component
- Fetches contact list from Apex class
- Prepares data in proper format
- Send data to GoogleMaps.cmp to draw Google Map
- This component will be embedded on Account page (only; restricted by .design file) to show all the Contacts on Google Map

DemoApp.app
- Fetches contact list from Apex class
- Prepares data in proper format
- Send data to GoogleMaps.cmp to draw Google Map

## Architecture
![Architecture](https://raw.githubusercontent.com/jrattanpal/Blog-GoogleMapsSample/master/Resources/Assets/GoogleMapsLightningComponents-Architecture.png?new=2)
