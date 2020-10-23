
# COVID-19 and Safety On Wheels in Chicago: 
## Let crashes show you how to learn lessons

![carechicago](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/traffic-highway_b.jpg)

![crashchicago](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/chicago-crashes.png)

<!-- 
![zipcode](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/chicago-zip-code-map-printable.jpg)
-->

# Data cleanness

* Obtaining

* Scrubbing

* Combining

* Cleaning

* Imputing

      - before cleaning & imputing:
    
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_1.png)
  
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_2.png)  
  
      - after cleaning & imputing:
      
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_4.png)  
  
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_5.png)
      
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_3.png)
  
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_6.png)  
  
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_7.png)
      
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_8.png)
  
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_9.png)
      
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_10.png)
  
  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_12.png)

  ![cleanness](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ0_11.png)

* Encoding

# Data exploration 

* Exploring

 **EDA Q1: What are Top 10 features yielding most information regarding crash causes and fatal degree levels?**

    * Analysis:
    
      <1> Fatal Degree Class-0
      
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_1.png)
      
      <2> Fatal Degree Class-1
      
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_2.png)
      
      <3> Fatal Degree Class-2
      
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_3.png)
      
      <4> Fatal Degree Class-3
      
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_4.png)

    * Recommendations:
      
        - LIGHTING_CONDITION {'DAYLIGHT': 1, 'DARKNESS_LIGHTED_ROAD': 2, 'DARKNESS': 3, 'DUSK': 4, 'DAWN': 5}
       
        - ROADWAY_SURFACE_COND {'DRY': 1, 'WET': 2, 'SNOW_OR_SLUSH': 3}
       
        - WEATHER_CONDITION {'CLEAR': 1, 'RAIN': 2, 'CLOUDY_OVERCAST': 3, 'SNOW': 4, 'OTHER': 5, 'FREEZING_RAIN_DRIZZLE': 6, 
                             'FOG_SMOKE_HAZE': 7}
       
        - TRAVEL_DIRECTION {'S': 1, 'W': 2, 'N': 3, 'E': 4, 'SE': 5, 'SW': 6, 'NW': 7, 'NE': 8}
       
        - INTERSECTION_RELATED {'Y': 1, 'N': 0}
       
        - FIRST_CONTACT_POINT {'OTHER': 1, 'REAR_LEFT': 2, 'TOTAL_ALL_AREAS': 3, 'FRONT': 4, 'ROOF': 5, 
                               'SIDE_RIGHT': 6, 'SIDE_LEFT': 7, 'REAR': 8, 'FRONT_LEFT': 9, 'REAR_RIGHT': 10, 
                               'FRONT_RIGHT': 11, 'UNDER_CARRIAGE': 12}
       
        - TRAFFIC_CONTROL_DEVICE {'TRAFFIC_SIGNAL': 1, 'STOP_SIGN_FLASHER': 2, 'OTHER': 3, 
                                  'FLASHING_CONTROL_SIGNAL': 4, 'YIELD': 5, 
                                  'PEDESTRIAN_CROSSING_SIGN': 6}
       
        - HIT_AND_RUN {'Y' : 1, 'N' : 0}
       
        - VEHICLE_TYPE {'PASSENGER': 1, 'SPORT_UTILITY_VEHICLE_SUV': 2, 'VAN_MINI_VAN': 3, 
                        'PICKUP': 4, 'BUS_OVER_15_PASS': 5, 'MOTORCYCLE_OVER_150CC': 6, 
                        'TRUCK_SINGLE_UNIT': 7, 'TRACTOR_WSEMI_TRAILER': 8, 'OTHER': 9, 
                        'TRACTOR_W_O_SEMI_TRAILER': 10, 'BUS_UP_TO_15_PASS': 10, 
                        'ALL_TERRAIN_VEHICLE_ATV': 11, 'SINGLE_UNIT_TRUCK_WITH_TRAILER': 12, 
                        'MOPED_OR_MOTORIZED_BICYCLE': 13, 'AUTOCYCLE': 13}
       
        - MANEUVER {'STRAIGHT_AHEAD': 1, 'TURNING_LEFT': 2, 'SLOW_STOP_IN_TRAFFIC': 3, 
                    'TURNING_RIGHT': 4, 'PARKED': 5, 'PASSING_OVERTAKING': 6, 'OTHER': 7, 
                    'CHANGING_LANES': 8, 'STARTING_IN_TRAFFIC': 9, 'BACKING': 10, 
                    'DRIVING_WRONG_WAY': 11, 'U_TURN': 12, 'MERGING': 13, 
                    'AVOIDING_VEHICLES_OBJECTS': 13, 'SKIDDING_CONTROL_LOSS': 14, 
                    'TURNING_ON_RED': 15, 'ENTER_FROM_DRIVE_ALLEY': 16, 
                    'ENTERING_TRAFFIC_LANE_FROM_PARKING': 17, 'DIVERGING': 18}
                    
        - UNIT_TYPE {'DRIVER': 1, 'PARKED': 2, 'DRIVERLESS': 3}
        
    * Future Work:
                    
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
  **EDA Q2: Over COVID-19 outbreak, why did traffic accidents still take place, if Illinois Stay at Home order took effect on March 21st, 2020?**

    * Analysis:
    
     <1> Fatal Degree Class-0

   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_11.png)
   
        - Lighting condition
        {'DAYLIGHT': 1, 'DARKNESS_LIGHTED_ROAD': 2, 'DARKNESS': 3, 'DUSK': 4, 'DAWN': 5}
        
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_111.png)    
   
        - Weather condition
        {'CLEAR': 1, 'RAIN': 2, 'CLOUDY_OVERCAST': 3, 'SNOW': 4, 'OTHER': 5, 'FREEZING_RAIN_DRIZZLE': 6, 
         'FOG_SMOKE_HAZE': 7}
        
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_112.png)  
   
        - Roadway surface condition
        {'DRY': 1, 'WET': 2, 'SNOW_OR_SLUSH': 3}
        
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_113.png)  
        
        - Intersection-related
        {'Y': 1, 'N': 0}
        
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_114.png) 
   
        - Travel direction
        {'S': 1, 'W': 2, 'N': 3, 'E': 4, 'SE': 5, 'SW': 6, 'NW': 7, 'NE': 8}
        
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_115.png)  
        
        - Maneuver
         {'STRAIGHT_AHEAD': 1, 'TURNING_LEFT': 2, 'SLOW_STOP_IN_TRAFFIC': 3, 
         'TURNING_RIGHT': 4, 'PARKED': 5, 'PASSING_OVERTAKING': 6, 'OTHER': 7, 
         'CHANGING_LANES': 8, 'STARTING_IN_TRAFFIC': 9, 'BACKING': 10, 
         'DRIVING_WRONG_WAY': 11, 'U_TURN': 12, 'MERGING': 13, 
         'AVOIDING_VEHICLES_OBJECTS': 13, 'SKIDDING_CONTROL_LOSS': 14, 
         'TURNING_ON_RED': 15, 'ENTER_FROM_DRIVE_ALLEY': 16, 
         'ENTERING_TRAFFIC_LANE_FROM_PARKING': 17, 'DIVERGING': 18}
        
   ![Top10class0](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_116.png)  

     <2> Fatal Degree Class-1
      
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_12.png)
   
        - Lighting condition
        {'DAYLIGHT': 1, 'DARKNESS_LIGHTED_ROAD': 2, 'DARKNESS': 3, 'DUSK': 4, 'DAWN': 5}
        
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_121.png)    
   
        - Weather condition
        {'CLEAR': 1, 'RAIN': 2, 'CLOUDY_OVERCAST': 3, 'SNOW': 4, 'OTHER': 5, 'FREEZING_RAIN_DRIZZLE': 6, 
         'FOG_SMOKE_HAZE': 7}
        
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_122.png)   
   
        - Roadway surface condition
        {'DRY': 1, 'WET': 2, 'SNOW_OR_SLUSH': 3}
        
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_123.png) 
   
        - Intersection-related
        {'Y': 1, 'N': 0}
        
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_124.png) 
   
        - Travel direction
        {'S': 1, 'W': 2, 'N': 3, 'E': 4, 'SE': 5, 'SW': 6, 'NW': 7, 'NE': 8}
        
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_125.png)      
        
        - Maneuver
         {'STRAIGHT_AHEAD': 1, 'TURNING_LEFT': 2, 'SLOW_STOP_IN_TRAFFIC': 3, 
         'TURNING_RIGHT': 4, 'PARKED': 5, 'PASSING_OVERTAKING': 6, 'OTHER': 7, 
         'CHANGING_LANES': 8, 'STARTING_IN_TRAFFIC': 9, 'BACKING': 10, 
         'DRIVING_WRONG_WAY': 11, 'U_TURN': 12, 'MERGING': 13, 
         'AVOIDING_VEHICLES_OBJECTS': 13, 'SKIDDING_CONTROL_LOSS': 14, 
         'TURNING_ON_RED': 15, 'ENTER_FROM_DRIVE_ALLEY': 16, 
         'ENTERING_TRAFFIC_LANE_FROM_PARKING': 17, 'DIVERGING': 18}
        
   ![Top10class1](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_126.png)  
      
     <3> Fatal Degree CLass-2
      
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_13.png)
   
        - Lighting condition
        {'DAYLIGHT': 1, 'DARKNESS_LIGHTED_ROAD': 2, 'DARKNESS': 3, 'DUSK': 4, 'DAWN': 5}
        
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_131.png)
             
        - Weather condition
        {'CLEAR': 1, 'RAIN': 2, 'CLOUDY_OVERCAST': 3, 'SNOW': 4, 'OTHER': 5, 'FREEZING_RAIN_DRIZZLE': 6, 
         'FOG_SMOKE_HAZE': 7}
        
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_132.png)
   
        - Roadway surface condition
        {'DRY': 1, 'WET': 2, 'SNOW_OR_SLUSH': 3}
   
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_133.png)
        
        - Intersection-related
        {'Y': 1, 'N': 0}
   
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_134.png)
        
        - Travel direction
        {'S': 1, 'W': 2, 'N': 3, 'E': 4, 'SE': 5, 'SW': 6, 'NW': 7, 'NE': 8}
        
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_135.png)
   
        - Maneuver
         {'STRAIGHT_AHEAD': 1, 'TURNING_LEFT': 2, 'SLOW_STOP_IN_TRAFFIC': 3, 
         'TURNING_RIGHT': 4, 'PARKED': 5, 'PASSING_OVERTAKING': 6, 'OTHER': 7, 
         'CHANGING_LANES': 8, 'STARTING_IN_TRAFFIC': 9, 'BACKING': 10, 
         'DRIVING_WRONG_WAY': 11, 'U_TURN': 12, 'MERGING': 13, 
         'AVOIDING_VEHICLES_OBJECTS': 13, 'SKIDDING_CONTROL_LOSS': 14, 
         'TURNING_ON_RED': 15, 'ENTER_FROM_DRIVE_ALLEY': 16, 
         'ENTERING_TRAFFIC_LANE_FROM_PARKING': 17, 'DIVERGING': 18}
        
   ![Top10class2](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_136.png)
      
     <4> Fatal Degree Class-3

   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_14.png)
   
        - Lighting condition
        {'DAYLIGHT': 1, 'DARKNESS_LIGHTED_ROAD': 2, 'DARKNESS': 3, 'DUSK': 4, 'DAWN': 5}
        
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_141.png)
        
        - Weather condition
        {'CLEAR': 1, 'RAIN': 2, 'CLOUDY_OVERCAST': 3, 'SNOW': 4, 'OTHER': 5, 'FREEZING_RAIN_DRIZZLE': 6, 
         'FOG_SMOKE_HAZE': 7}
        
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_142.png) 
   
        - Roadway surface condition
        {'DRY': 1, 'WET': 2, 'SNOW_OR_SLUSH': 3}
        
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_143.png) 
   
        - Intersection-related
        {'Y': 1, 'N': 0}
   
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_144.png) 
        
        - Travel direction
        {'S': 1, 'W': 2, 'N': 3, 'E': 4, 'SE': 5, 'SW': 6, 'NW': 7, 'NE': 8}
        
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_145.png)
    
        - Maneuver
         {'STRAIGHT_AHEAD': 1, 'TURNING_LEFT': 2, 'SLOW_STOP_IN_TRAFFIC': 3, 
         'TURNING_RIGHT': 4, 'PARKED': 5, 'PASSING_OVERTAKING': 6, 'OTHER': 7, 
         'CHANGING_LANES': 8, 'STARTING_IN_TRAFFIC': 9, 'BACKING': 10, 
         'DRIVING_WRONG_WAY': 11, 'U_TURN': 12, 'MERGING': 13, 
         'AVOIDING_VEHICLES_OBJECTS': 13, 'SKIDDING_CONTROL_LOSS': 14, 
         'TURNING_ON_RED': 15, 'ENTER_FROM_DRIVE_ALLEY': 16, 
         'ENTERING_TRAFFIC_LANE_FROM_PARKING': 17, 'DIVERGING': 18}
        
   ![Top10class3](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ1_146.png)

    * Recommendations:
    
        - Lighting condition : DAYLIGHT (major) , DARKNESS_LIGHTED_ROAD (second)
        
        - Weather condition : CLEAR (major) , RAIN (second)
        
        - Roadway surface condition : DRY (major) , WET (second)
        
        - Intersection-related : YES (major)
        
        - Travel direction : S W N E (equivalently major)
        
        - Maneuver : STRAIGHT_AHEAD (major) , TURNING_LEFT (second) , 
                     SLOW_STOP_IN_TRAFFIC (third) , TURNING_RIGHT (forth) , 
                     PARKED (fifth)
        

    * Future Work:

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 **EDA Q3: Following Q1, what're time-dependent? What're not? Any other factors possibly involved? What are they?**
 
    * Analysis:
    
      - Cash Hour
    
   | CRASH HOUR | SEX F  | SEX M  | SUM   |
   | :-----:    | :---:  | :---:  | :---: |
   |   0        | 1.231  | 1.333  | 2.564 |
   |   1        | 1.465  | 1.700  | 3.165 |
   |   2	    | 1.421	 | 1.286  | 2.707 |
   |   3	    | 1.448	 | 1.562  | 3.010 |
   |   4	    | 0.917	 | 1.846  | 2.763 |
   |   5	    | 1.667	 | 1.143  | 2.810 |
   |   6	    | 0.667	 | 1.364  | 2.031 |
   |   7        | 1.929	 | 1.529  | 3.458 |
   |   8        | 1.216  | 1.206  | 2.422 |
   |   9        | 1.364  | 0.906  | 2.270 |
   |  10        | 1.120  | 1.529  | 2.649 |
   |  11        | 1.303  | 1.044  | 2.347 |
   |  12        | 0.957  | 1.220  | 2.177 |
   |  13        | 0.893  | 0.857  | 1.750 |
   |  14        | 1.343  | 1.101  | 2.444 |
   |  15        | 1.068  | 1.129  | 2.197 |
   |  16        | 1.606  | 1.359  | 2.965 |
   |  17        | 1.174  | 1.576  | 2.750 |
   |  18        | 1.104  | 1.553  | 2.657 |
   |  19        | 1.333  | 1.192  | 2.525 |
   |  20        | 1.410  | 1.208  | 2.618 |
   |  21        | 1.175  | 1.670  | 2.845 |
   |  22        | 1.298  | 1.500  | 2.798 |
   |  23        | 1.226  | 0.912  | 2.138 |
   
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_11.png)   
   
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_4.png)

      - Cash Day of Week

   | CRASH DAY OF WEEk | SEX F  | SEX M  | SUM   |
   | :------------:    | :---:  | :---:  | :---: |
   |        1	     | 1.418  | 1.188  | 2.606 |
   |        2	     | 1.273  | 1.547  | 2.820 |
   |        3	     | 1.142  | 1.284  | 2.426 |
   |        4	     | 1.126  | 1.469  | 2.595 |
   |        5	     | 1.298  | 1.489  | 2.787 |
   |        6	     | 1.257  | 1.115  | 2.372 |
   |        7	     | 1.260  | 1.296  | 2.556 |
   
 ![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_12.png)
   
 ![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_5.png)
 
       - Cash Month
   
   | CRASH MONTH | SEX F  | SEX M  | SUM   |
   | :------:    | :---:  | :---:  | :---: |
   |    4	     | 1.529  | 1.253  | 2.782 |
   |    5	     | 1.387  | 1.352  | 2.739 |
   |    6	     | 1.128  | 1.441  | 2.569 |
   |    7	     | 1.195  | 1.175  | 2.370 |
   |    8	     | 1.196  | 1.477  | 2.673 |

![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_13.png)

![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_6.png)

       - Number of Units in Crash
       
   | Unit Num    | SEX F  | SEX M  | SUM   |
   | :---------: | :---:  | :---:  | :---: |     
   |    1	     | 1.667  | 2.000  | 3.667 |
   |    2	     | 1.232  | 1.276  | 2.508 |
   |    3	     | 1.276  | 1.420  | 2.696 |
   |    4	     | 1.145  | 1.184  | 2.329 |
   |    5	     | 2.500  | 3.000  | 5.500 |
   |    6	     | 1.500  | 1.667  | 3.167 |

![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_10.png)

       - Posted Speed Limit
              
![Info](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_1.png)
   
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_9.png)
   
       - Age
              
![Info](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_2.png)
   
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_7.png)
   
       - Vehicle Year
              
![Info](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_3.png)
   
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_8.png)

    
    * Recommendations:
    
![Info](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_18.png)

![Info](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_19.png)
    
       - Average Hour over Crash w.r.t. Damage Cost and Fatal Degree  
    
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_14.png)

       - Average Hour over Crash w.r.t. Damage Cost and Fatal Scenario (or Condition)

![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_15.png)

       - Average Unit over Crash w.r.t. Damage Cost and Fatal Degree  

![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_16.png)

       - Average Unit over Crash w.r.t. Damage Cost and Fatal Scenario (or Condition)

![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_17.png)

       - Average Day over Crash w.r.t. Damage Cost and Fatal Degree
       
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_20.png)

       - Average Day over Crash w.r.t. Damage Cost and Fatal Scenario (or Condition)
       
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_21.png)

       - Average Month over Crash w.r.t. Damage Cost and Fatal Degree
       
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_22.png)

       - Average Month over Crash w.r.t. Damage Cost and Fatal Scenario (or Condition)
       
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_23.png)

       - Average Fatal Degree over Crash w.r.t. Vehicle Make and Fatal Scenario
       
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_24.png)

       - Average Fatal Degree over Crash w.r.t. Vehicle Model and Fatal Scenario
       
![FATALDEGREE](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_EDAQ2_25.png)
    
    * Future Work:

# Data interpretation 

* Decision Tree (criterion = entropy) as baseline model

   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |    
   |    0	             | 99     | 7      | 4     |  7    |  117  |
   |    1	             | 3      | 82     | 11    |  10   |  106  |
   |    2                | 8      | 13     | 102   |  8    |  131  |
   |    3	             | 2      | 10     | 5     |  60   |  77   |
   |   All               | 112    | 112    | 122   |  85   |  431  |
   
   | multi-class    | precision     | recall     | f1-score     |  support    | 
   | :------------: | :-----------: | :--------: | :----------: | :---------: |  
   |    0	        | 0.883929      | 0.846154	 | 0.864629	    | 117.000000  |
   |    1	        | 0.732143	| 0.773585	 | 0.752294	    | 106.000000  |
   |    2	        | 0.836066	| 0.778626	 | 0.806324	    | 131.000000  |
   |    3	        | 0.705882	| 0.779221	 | 0.740741	    | 77.000000   |
   | accuracy	  | 0.795824	| 0.795824	 | 0.795824	    | 0.795824    |
   | macro avg	  | 0.789505	| 0.794396	 | 0.790997	    | 431.000000  |
   | weighted avg	  | 0.800242	| 0.795824	 | 0.797147	    | 431.000000  |

![DT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_DT_1.png)

![DT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_DT_2.png)

* Regression with CART tree

      - before model tuning, i.e. hyperparameter optimization and tree-pruning
      
   | statistics          | MAE    | MSE    | RMSE  | R^2   | 
   | :-----------------: | :---:  | :---:  | :---: | :---: | 
   |                     | 0.37   | 0.73   | 0.85  | 0.36  |
      
      - after model tuning, i.e. hyperparameter optimization and tree-pruning
      
   | statistics          | MAE    | MSE    | RMSE  | R^2   | 
   | :-----------------: | :---:  | :---:  | :---: | :---: | 
   |                     | 0.47   | 0.56   | 0.75  | 0.51  |
         
![CT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_CT_1.png)

![CT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_CT_2.png)

* Random Forest

  - Decision Tree (criterion = gini) as baseline model
  
  
   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |    
   |    0	             | 91     | 6      | 12    |  8    | 117   |
   |    1	             | 6      | 86     | 8     |  6    | 106   |
   |    2                | 11     | 11     | 102   |  7    | 131   |
   |    3	             | 10     | 7      | 3     |  57   | 77    |
   |   All               | 118    | 110    | 125   |  78   | 431   |
   
   | multi-class    | precision      | recall      | f1-score     |  support    | 
   | :------------: | :-----------:  | :--------:  | :----------: | :---------: |  
   |    0	        | 0.771186	 | 0.777778	   | 0.774468	| 117.000000  |
   |    1	        | 0.781818	 | 0.811321	   | 0.796296	| 106.000000  |
   |    2	        | 0.816000	 | 0.778626	   | 0.796875	| 131.000000  |
   |    3	        | 0.730769	 | 0.740260	   | 0.735484	| 77.000000   |
   | accuracy	  | 0.779582	 | 0.779582	   | 0.779582	| 0.779582    |
   | macro avg	  | 0.774943	 | 0.776996	   | 0.775781	| 431.000000  |
   | weighted avg	  | 0.780201	 | 0.779582	   | 0.779682	| 431.000000  |
  
![RF](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_RF_1.png)

    * Feature importance
    
![RF](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_RF_2.png)

  
  - Bagged Tree (criterion = gini) vs. Random Forest
  
   | Model Accuracy      | Train         | Test          | 
   | :-----------------: | :----------:  | :----------:  |    
   |    Bagged Tree	 | 99.63%        | 82.37%        | 
   |    Random Forest	 | 100.00%       | 89.33%        | 
   
   
      * Bagged (Bootstrap Aggregation) 
      
   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |    
   |  0	             | 95	    | 3	 | 13	   | 6     | 117   |
   |  1	             | 4	    | 88	 | 6	   | 8     | 106   |
   |  2	             | 6	    | 8	 | 111   | 6     | 131   |
   |  3	             | 5	    | 6	 | 5	   | 61    | 77    |
   | All	             | 110    | 105	 | 135   | 81    | 431   |
   
   | multi-class    | precision      | recall      | f1-score     |  support    | 
   | :------------: | :-----------:  | :--------:  | :----------: | :---------: |  
   | 0	        | 0.863636	 | 0.811966	   | 0.837004	| 117.000000  |
   | 1	        | 0.838095	 | 0.830189	   | 0.834123	| 106.000000  |
   | 2	        | 0.822222	 | 0.847328	   | 0.834586	| 131.000000  |
   | 3	        | 0.753086	 | 0.792208	   | 0.772152	| 77.000000   |
   | accuracy	  | 0.823666	 | 0.823666	   | 0.823666	| 0.823666    |
   | macro avg	  | 0.819260	 | 0.820423	   | 0.819466	| 431.000000  |
   | weighted avg	  | 0.825017	 | 0.823666	   | 0.823975	| 431.000000  | 
   
![RF](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_RF_4.png)
      
      * Random Forest
      
   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |   
   | 0	             | 101    | 4	 | 9	   | 3     | 117   |
   | 1	             | 3	    | 97	 | 3	   | 3     | 106   |
   | 2	             | 1	    | 5	 | 122   | 3     | 131   |
   | 3	             | 1	    | 2	 | 6	   | 68    | 77    |
   | All	             | 106    | 108	 | 140   | 77    | 431   |
   
   | multi-class    | precision      | recall      | f1-score     |  support    | 
   | :------------: | :-----------:  | :--------:  | :----------: | :---------: |  
   | 0	        | 0.952830	 | 0.863248	   | 0.905830	| 117.000000  |
   | 1	        | 0.898148	 | 0.915094	   | 0.906542	| 106.000000  |
   | 2	        | 0.871429	 | 0.931298	   | 0.900369	| 131.000000  |
   | 3	        | 0.883117	 | 0.883117	   | 0.883117	| 77.000000   |
   | accuracy	  | 0.900232	 | 0.900232	   | 0.900232	| 0.900232    |
   | macro avg	  | 0.901381	 | 0.898189	   | 0.898964	| 431.000000  |
   | weighted avg	  | 0.902186	 | 0.900232	   | 0.900287	| 431.000000  |
     
![RF](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_RF_5.png)
   
            - Feature importance (based on Random Forest)
    
![RF](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_RF_3.png)

* Ada/Gradient Boost

      - AdaBoost Mean Adaboost Cross-Val Score (k=30): 63.30%
      
   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |    
   |  0	             | 89	    | 10	 | 14	   | 4     | 117   |
   |  1	             | 2	    | 64	 | 23	   | 17    | 106   |
   |  2	             | 11	    | 24	 | 84	   | 12    | 131   |
   |  3	             | 1	    | 15	 | 16	   | 45    | 77    |
   | All	             | 103    | 113	 | 137   | 78    | 431   |
   
   | multi-class    | precision      | recall      | f1-score     |  support    | 
   | :------------: | :-----------:  | :--------:  | :----------: | :---------: |  
   | 0	        | 0.864078	 | 0.760684	   | 0.809091	| 117.000000  |
   | 1	        | 0.566372	 | 0.603774	   | 0.584475	| 106.000000  |
   | 2	        | 0.613139	 | 0.641221	   | 0.626866	| 131.000000  |
   | 3	        | 0.576923	 | 0.584416	   | 0.580645	| 77.000000   |
   | accuracy	  | 0.654292	 | 0.654292	   | 0.654292	| 0.654292    |
   | macro avg	  | 0.655128	 | 0.647524	   | 0.650269	| 431.000000  |
   | weighted avg	  | 0.663287	 | 0.654292	   | 0.657650	| 431.000000  |

![ADABT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_ADABT_1.png)  

      - Gradient Boost Mean GBT Cross-Val Score (k=30): 70.41%
      
   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |   
   |  0	             | 93	    | 6	 | 14	   | 4     | 117   |
   |  1	             | 1	    | 91	 | 5	   | 9     | 106   |
   |  2	             | 1	    | 14	 | 106   | 10    | 131   |
   |  3	             | 1	    | 3	 | 6	   | 67    | 77    |
   | All	             | 96	    | 114	 | 131   | 90    | 431   |
   
   | multi-class    | precision      | recall      | f1-score     |  support    | 
   | :------------: | :-----------:  | :--------:  | :----------: | :---------: |  
   |  0	        | 0.968750	 | 0.794872	   | 0.873239	| 117.000000  |
   |  1	        | 0.798246	 | 0.858491	   | 0.827273	| 106.000000  |
   |  2	        | 0.809160	 | 0.809160	   | 0.809160	| 131.000000  |
   |  3	        | 0.744444	 | 0.870130	   | 0.802395	| 77.000000   |
   | accuracy	  | 0.828306	 | 0.828306	   | 0.828306	| 0.828306    |
   | macro avg	  | 0.830150	 | 0.833163	   | 0.828017	| 431.000000  |
   | weighted avg	  | 0.838237	 | 0.828306	   | 0.829801	| 431.000000  |

![GBT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_GBT_1.png)

* XGBoost

      Grid Search found the following optimal parameters:

            - learning_rate: 0.1 
            
            - max_depth: 6 
            
            - min_child_weight: 10 
            
            - n_estimators: 100 
            
            - subsample: 0.7 
            
            - Training Accuracy: 94.79% 
            
            - Validation accuracy: 95.13%

   | True / Predicted    | 0      | 1      | 2     |  3    |  All  |
   | :-----------------: | :---:  | :---:  | :---: | :---: | :---: |
   |  0	             | 107    | 2	 | 4	   | 4     | 117   |
   |  1	             | 0	    | 105	 | 0	   | 1     | 106   |
   |  2	             | 1	    | 3	 | 125   | 2     | 131   |
   |  3	             | 0	    | 1	 | 3	   | 73    | 77    |
   | All	             | 108    | 111	 | 132   | 80    | 431   |   
   
   | multi-class    | precision      | recall      | f1-score     |  support    | 
   | :------------: | :-----------:  | :--------:  | :----------: | :---------: |  
   | 0	        | 0.990741	 | 0.914530	   | 0.951111	| 117.000000  |
   | 1	        | 0.945946	 | 0.990566	   | 0.967742	| 106.000000  |
   | 2	        | 0.946970	 | 0.954198	   | 0.950570	| 131.000000  |
   | 3	        | 0.912500	 | 0.948052	   | 0.929936	| 77.000000   |
   | accuracy	  | 0.951276	 | 0.951276	   | 0.951276	| 0.951276    |
   | macro avg	  | 0.949039	 | 0.951837	   | 0.949840	| 431.000000  |
   | weighted avg	  | 0.952442	 | 0.951276	   | 0.951254	| 431.000000  |
  
![XGBT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_XGBT_1.png)
   
      - Feature importance (based on XGBoost)
    
![XGBT](https://github.com/renjmindy/dsc-mod-3-project-v2-1-onl01-dtsc-ft-052620/blob/master/images/mod3_XGBT_2.png)
