---
sidebar_position: 7
title:  Tracks and Routes
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/_buttonAndroidStore.mdx';
import AppleStore from '@site/src/components/_buttonAppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';

OsmAnd has many powerful features to display various routes on the map. Routes could be built as part of Navigation, created via Plan Route, imported as GPX tracks, recorded via Trip Recording plugin or browsed and selected from OpenStreetMap data.

## Type of routes on the map

OsmAnd can display several different type of routes:

1.  [Tracks (GPX)](#tracks) - recorded or planned trip saved in [GPX-format](https://en.wikipedia.org/wiki/GPS_Exchange_Format). This kind of route could be imported from the external source, created in the application or recorded by user. GPX could contain one of 3 different types of data or all of them:
    - Track as a line - file has ```<trkpt>``` points array, each point has location and optionally time, speed, altitude and other attributes. These tracks are displayed on the map as solid lines.
    - Track as a route -  file has ```<rtept>``` points array, each point described as an intermediate point of the route. It depends on how points within a route should be connected either as small route segments or via straight line. These tracks are displayed on the map as dashed lines. 
    - Waypoints - file has ```<wpt>``` points with attributes. Waypoints are displayed as circular points on the map. You could click on them to get additional information.
2. [Navigation Route](#navigation-route) - a route line displayed during [navigation](/docs/documentation/navigation/route-navigation). By default this is a solid transparent blue line, though default appearance depends on [vector map style](/docs/documentation/map/vector-maps#default-map-styles), [day & night mode](/docs/documentation/map/vector-maps#map-mode). It's also possible to fully customize it on Android.
3. [Routes and route networks on the map](#routes-on-the-map) - special [objects](/docs/documentation/map/vector-maps#routes) on the map from [OpenStreetMap](https://wiki.openstreetmap.org/wiki/Relation:route) data and provided with standard vector maps. They typically represent popular local routes and could be displayed in many ways (shields, color, thickness, pattern). To use these types of routes you will need to enable them on the map.

Read more about [GPX Tracks](/docs/documentation/personal/tracks#track).

## Tracks 

There are two options to display [Tracks](/docs/documentation/personal/tracks) on the map: via [<Translate android="true" ids="configure_map"/>](/docs/documentation/map/tracks-on-map#display-via-configure-map-menu) menu or [<Translate android="true" ids="shared_string_my_places"/>](/docs/documentation/map/tracks-on-map#display-via-my-places-menu) menu

![Tracks on the map Android](@site/static/img/map/tracks_layer_android.png) ![Tracks on the map iOS](@site/static/img/map/tracks_layer_ios.png) 

### Display via <Translate ios="true" ids="configure_map"/> menu

<Translate android="true" ids="android_button_seq"/> <Translate android="true" ids="shared_string_menu,configure_map,show_gpx"/> → &#8230; → Choosing tracks for display from the list and setting track appearance.

<p> </p>

<Translate ios="true" ids="ios_button_seq"/> <Translate ios="true" ids="menu,configure_map,tracks"/> → Choosing tracks for displayed from the list.

<Tabs groupId="operating-systems">

<TabItem value="def" label="Default" default>

![Tracks menu Android](@site/static/img/map/tracks_menu_android.png) ![Tracks menu iOS](@site/static/img/map/tracks_menu_ios.png)  

</TabItem>

<TabItem value="android" label="Android">

![Tracks menu Android](@site/static/img/map/tracks_menu_android.png) 

</TabItem>

<TabItem value="ios" label="iOS">

![Tracks menu iOS](@site/static/img/map/tracks_menu_ios.png) 

</TabItem>

</Tabs>

### Display via <Translate android="true" ids="shared_string_my_places"/> menu

&nbsp;<Translate android="true" ids="android_button_seq"/> <Translate android="true" ids="shared_string_menu,shared_string_my_places,shared_string_gpx_files"/> → &#8942; → <Translate android="true" ids="hared_string_show_on_map"/> or ["Map" button](/docs/documentation/personal/tracks#my-places-android) for choosing multiple tracks.

<p> </p>

&nbsp;<Translate ios="true" ids="ios_button_seq"/> <Translate ios="true" ids="menu,menu_my_places,tracks"/> → &#8250; → <Translate ios="true" ids="map_settings_show"/> or ["Layer" button](/docs/documentation/personal/tracks#my-places-ios) for choosing multiple tracks.

<Tabs groupId="operating-systems">

<TabItem value="def" label="Default" default>

![Tracks my places Android](@site/static/img/map/tracks_myplaces_android.png) ![Tracks menu iOS](@site/static/img/map/tracks_myplaces_ios.png)

</TabItem>

<TabItem value="android" label="Android">

![Tracks my places Android](@site/static/img/map/tracks_myplaces_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Tracks menu iOS](@site/static/img/map/tracks_myplaces_ios.png)

</TabItem>

</Tabs>

### Track Appearance

In OsmAnd you can change the color, the thickness of the track, display arrows and icons of the starting and ending points.

To get to the track Appearance menu, you need to display track on the map, then in the [Track Context menu](https://docs.osmand.net/en/main@latest/docs/documentation/map/track-context-menu#overview) in the <Translate android="true" ids="shared_string_overview"/> section, [shortcut](/docs/documentation/map/map-context-menu#select-route-short-tap-for-android) is to click on the "palette" icon. 

 <Tabs groupId="operating-systems">

<TabItem value="def" label="Default" default>

![Track menu options Android](@site/static/img/map/eye_button_android.png) ![Track menu iOS](@site/static/img/map/eye_button_ios.png)

</TabItem>

<TabItem value="android" label="Android">

![Track menu options Android](@site/static/img/map/eye_button_android.png) ![Track menu Appearance Android](@site/static/img/map/track_appearance_menu_android.png) 

</TabItem>

<TabItem value="ios" label="iOS">

![Track menu iOS](@site/static/img/map/eye_button_ios.png) ![Configure color iOS](@site/static/img/map/track_appearance_menu_ios.png) 

</TabItem>

</Tabs>

|**Parameter and Description**|   
|------------|
|**<Translate android="true" ids="gpx_split_interval"/>** - splits track into intervals by **_Distance_** or **_Time_** and displays shields on the map.|
|![Track menu Appearance Split interval Android](@site/static/img/map/track_appearance_menu_split_interval_android.png)| 
|**<Translate android="true" ids="gpx_direction_arrows"/>** - adds direction info on the track.|
|![Track menu Appearance direction arrows Android](@site/static/img/map/track_appearance_menu_direction_arrows_android.png)|  
|**<Translate android="true" ids="track_show_start_finish_icons"/>** - shows or hides start/finish icons of the track segments.|
|![Track menu Appearance start and finish icons Android](@site/static/img/map/track_appearance_menu_sf_icons_android.png)|  
|**<Translate android="true" ids="shared_string_color"/>** -  changes the color (solid or gradient) of the track using internal data: **_Solid Color_**, **_Height_**, **_Speed_**, **_Slope_** (PRO feature), **_Smoothness_** (OsmAnd plan route), **_Surface_** (OsmAnd plan route). If necessary data is not available grey color is displayed. |
|![Track menu Appearance Track color Android](@site/static/img/map/track_appearance_menu_track_color_android.png)|
|**<Translate android="true" ids="select_track_width"/>** - changes the thickness for the track between **_<Translate android="true" ids="rendering_value_thin_name"/>_**, **_<Translate android="true" ids="rendering_value_medium_name"/>_**, **_<Translate android="true" ids="rendering_value_bold_name"/>, <Translate android="true" ids="shared_string_custom"/>_**.|
|![Track menu Appearance Track Thickness Android](@site/static/img/map/track_appearance_menu_track_thickness_android.png)|

### Analyze Track on Map (Android)

This option allows you to interactively review track information using graphs and the map. To get access to this menu shortly tap on the track → [<Translate android="true" ids="shared_string_options"/>](/docs/documentation/map/track-context-menu#options) → <Translate android="true" ids="analyze_on_map"/>

![Track menu analyze on map Android](@site/static/img/personal/tracks/track_analyze_on_map_android.png) ![Track menu analize on the map distance Android](@site/static/img/personal/tracks/track_analyze_on_map_distance_android.png) 

- **Graph data**: Altitude / Slope / Speed (if data is available in the track).
- **Graph dimension**: Distance / Time.
- **Tap/Slide**: tap to Graph for showing info about track point and moving along Graph highlights point location on the map and displays info about point on the bar.
- **Scale**: scale Graph by [two fingers gesture](/docs/documentation/map/interact-with-map#gestures). 
- **Follow My location**: click button [My Location](/docs/documentation/map/interact-with-map#my-location--zoom), so map view and graph is synchronized with your location. In that case **graph scale** will stay constant and **bar information** will be fixed to 1/4 from the left. As you move, **graph will slide** from left to right displaying information Ahead of your Track. This functionality is useful for hiking & cycling during navigation, though this screen doesn't have other widgets displayed.


![Track menu analyze on map 3 Android](@site/static/img/personal/tracks/track_analyze_on_map_3_android.png) ![Track menu analyze on map 5 Android](@site/static/img/personal/tracks/track_analyze_on_map_5_android.png)


<!-- 
![Track menu analyze on map 3 Android](@site/static/img/personal/tracks/track_analyze_on_map_3_android.png) ![Track menu analyze on map 4 Android](@site/static/img/personal/tracks/track_analyze_on_map_4_android.png)
![Track menu analyze on map 1 Android](@site/static/img/personal/tracks/track_analyze_on_map_1_android.png) ![Track menu analyze on map 1.1 Android](@site/static/img/personal/tracks/track_analyze_on_map_1.1_android.png)
![Track menu analyze on map 2 Android](@site/static/img/personal/tracks/track_analyze_on_map_2_android.png) ![Track menu analyze on map 2.1 Android](@site/static/img/personal/tracks/track_analyze_on_map_2.1_android.png)
![Track menu analyze on map 5 Android](@site/static/img/personal/tracks/track_analyze_on_map_5_android.png)
-->

## Navigation Route

Navigation route is a solid line prepared by [Route Preparation process](/docs/documentation/navigation/route-navigation). It is displayed during Navigation or during Route preparation step.

 ![Route on the map Android](@site/static/img/map/route_layer_android.png) ![Route on the map iOS](@site/static/img/map/route_layer_ios.png)

### Route Appearance (Android)

You can customize the route line's appearance for any navigation profile differently. It is possible to select **_Color_** and **_Width_** for the line, **separately** for **_Day_** and **_Night_** [mode](/docs/documentation/map/vector-maps#map-mode).

<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2,customize_route_line"/>

<p> </p>

![Route Customization Android](@site/static/img/map/route_custom_android.png)

## Routes on the map

 

OsmAnd can highlight [routes present on OpenStreetMap](https://wiki.openstreetmap.org/wiki/Relation:route). They are not selectable but with the right configuration of visible set of routes, it's possible to follow the route by color & shields, you can create a Track on top of the routes using [Plan Route](/docs/documentation/plan-route/create-route) functionality.


<Translate android="true" ids="android_button_seq"/> <Translate android="true" ids="shared_string_menu,configure_map,map_widget_map_rendering,rendering_category_routes"/>

<p> </p>

<Translate ios="true" ids="ios_button_seq"/> <Translate ios="true" ids="menu,configure_map,map_settings_style,rendering_category_routes"/>

<p> </p>

**Read more** about Map Routes at [Vector map style](/docs/documentation/map/vector-maps#routes).

 <Tabs groupId="operating-systems">

<TabItem value="def" label="Default" default>

![Configure Map Routes section](@site/static/img/map/configure_map_routes_android.png) 

</TabItem>

<TabItem value="android" label="Android">

![Configure Map Routes section](@site/static/img/map/configure_map_routes_android.png) 

</TabItem>

<TabItem value="ios" label="iOS">

![Track menu iOS](@site/static/img/map/configure_map_routes_ios.png) 

</TabItem>

</Tabs>


![Map routes - hiking osmc](@site/static/img/map/map-routes-hiking-osmc.png)![Map routes - cycle-node-networks](@site/static/img/map/map-routes-cycle-node-networks.png)


## Read more



[Track Context menu](/docs/documentation/map/track-context-menu)

[Configure map](/docs/documentation/map/configure-map-menu)

[Navigation by track](/docs/documentation/navigation/gpx-navigation)

[GPX tracks](/docs/documentation/personal/tracks)

[Tracks on the map](/docs/documentation/map/tracks-on-map)

[Plan route](/docs/documentation/plan-route)

[Trip Recording](/docs/documentation/plugins/trip-recording)

[Analyze on Map](/docs/documentation/map/tracks-on-map)
