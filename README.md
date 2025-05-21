## Relevant Data Points

| Data Point Name | Description | Type |
| --- | --- | --- |
| mode_code | Aircraft state | enum_int: {"0":"Standby","1":"Takeoff preparation","2":"Takeoff preparation completed","3":"Manual flight","4":"Automatic takeoff","5":"Wayline flight","6":"Panoramic photography","7":"Intelligent tracking","8":"ADS-B avoidance","9":"Auto returning to home","10":"Automatic landing","11":"Forced landing","12":"Three-blade landing","13":"Upgrading","14":"Not connected","15":"APAS","16":"Virtual stick state","17":"Live flight Controls","18":"Airborne RTK fixing mode"} |
| mode_code_reason | The reason the aircraft entered the current state | enum_int: {"0":"No meaning","1":"Insufficient battery power (return, landing)","2":"Insufficient battery voltage (return, landing)","3":"Severely low voltage (return, landing)","4":"Requested by remote controller buttons (takeoff, return, landing)","5":"Requested by App (takeoff, return, landing)","6":"Loss of remote controller signal (return, landing, hover)","7":"Triggered by external devices such as navigation, SDK, etc. (takeoff, return, landing)","8":"Entered the dock GEO Zone (landing)","9":"Although a return was triggered, it was too close to the Home point (landing)","10":"Although a return was triggered, it was too far from the Home point (landing)","11":"Requested when executing waypoint missions (takeoff)","12":"Requested after reaching above the Home point in the return phase (landing)","13":"Continued descent after the aircraft's height dropped to 0.7m from the ground (second-stage descent limit) leading to (landing)","14":"Forced breakthrough of low altitude protection by devices like App, SDK (landing)","15":"Requested due to passing flights in the vicinity (returning, landing)","16":"Requested due to height control failure (return, landing)","17":"Entered after intelligent low battery return (landing)","18":"AP controls the flight mode (manual flight)","19":"Hardware abnormally (return, landing)","20":"End of anti-collision protection (landing)","21":"Return canceled (hover)","22":"Encountered obstacles during the return (landing)"} |
| cameras | Aircraft camera information | JSON object that contains remain_photo_num, reamin_record_duration, record_time, camera_mode, photo_state, and recording_state |
| reamin_photo_num | Remaining number of photos to take | int |
| remain_record_duration | Remaining recording time | int |
| record_time | Video recording duration | int |
| camera_mode | Camera mode | enum_int: {"0":"Capturing","1":"Recording","2":"Smart Low-Light","3":"Panoramic photography"} |
| photo_state | Photo capturing status | enum_int: {"0":"Idle","1":"Capturing photo"} |
| recording_state | Recording state | enum_int: {"0":"Idle","1":"Recording"} |
| is_near_area_limit | Whether approaching the GEO Zone | enum_int: {"0":"Not reaching the GEO Zone","1":"Approaching the GEO Zone"} |
| is_near_height_limit | Whether approaching the set height limit | enum_int: {"0":"Not reaching the set height limit","1":"Approaching the set height limit"} |
| height_limit | Aircraft height limit | int |
| storage | Storage capactiy | JSON object that contains total and used |
| total | Total storage capacity | int: {"unit_name":"Kilobytes / KB"} |
| used | Total used storaage capacity | int: {"unit_name":"Kilobytes / KB"} |
| battery | Aircraft battery information | JSON object that contains capacity_percent, remain_flight_time, and return_home_power |
| capacity_percent | Total remaining battery capacity | int: {"max":100,"min":0} |
| remain_flight_time | Remaining flight time | int: {"unit_name":"Seconds / s"} |
| return_home_power | Percentage of power required for return home | int: {"max":100,"min":0} |
| total_flight_distance | Accumulated total mileage of the aircraft | float: {"unit_name":"Meters / m"} |
| total_flight_time | Accumulated total flight time of the aircraft | int: {"unit_name":"Seconds / s"} |
| home_distance | Distance from the Home point | float |
| home_latitude | Home point latitude | float |
| home_longitude | Home point longitude | float |
| elevation | Relative takeoff point altitude | float |
| height | Absolute height | float |
| latitude | Current latitude | float: {"max":"3.4028235E38","min":"-1.4E-45","step":"0.1"} |
| longitude | Current longitude | float: {"max":"3.4028235E38","min":"-1.4E-45","step":"0.1"} |