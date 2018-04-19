what happens when  we launch this component on Android  Lolipop version or bellow without enabling GPS.
```xml
// AndroidManifest.xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```
```js
export default class App extends Component {  
  
    constructor() {  
        super();  
		this.state = {  
			latitude: 33.333,  
			longitude: 33.33,  
		  }  
    }  
  
    render() {  
        return (  
            <View>  
			 <Text>Latitude : {this.state.latitude}</Text>  
			 <Text>Longitude : {this.state.longitude}</Text>  
		 </View>  
		 );  
	  }  
    setCoods(position){  
        this.setState({  
	      latitude: position.coords.latitude,
	      longitude:position.coords.longitude,  
		  });  
     }  
  
    async componentDidMount() {  
        console.log("componentDidMount");  
		const granted = await PermissionsAndroid.request(  
				PermissionsAndroid.PERMISSIONS.ACCESS_FINE_LOCATION, {  
                title: 'App needs to access your location',  
				message: 'App needs access to your location for #100DaysOfReact'}  
        );  
  
		if (granted) {  
		  navigator.geolocation.getCurrentPosition(  
                (position) => {  
                    console.log("position",position);  
		  this.setCoods(position) });  
		  }
    }  
}
```
