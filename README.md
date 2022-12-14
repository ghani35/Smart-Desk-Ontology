# Smart-Desk-Ontology
In this repository you can find a simple example about Ambient Intelligence applicaitons which is  **A smart desk**. The application is built as a topological onotology on Protegé.

# Protegé
[Protegé](https://protege.stanford.edu/) is A free, open-source ontology editor and framework for building intelligent systems

# What is a smart desk?
Smart desk is a desk that allows you to complete your work or study in a more comfortable way by providing you with a set of smart features that minimize the workload, the time management and extend the working period. Also, it can recognize some activities that you are doing, as well as give you some useful suggestions.

# Topological Ontology 
It is build by defining **Entities, data properties, object properties and SWRL rules**, the reasoner used is **Pallet**

## Entities
Here is the list of classes and sub-classes used in this ontology 
  * DeskComponent:  The component of the smart desk which are Chair and Desk 
  * DeskFeatures: The features provided (actions done) by the smart desk which are executed based on a specific condition. They are codded by SWRL rules.
  * DeskSuggestion: A list of smart suggestions by the desk 
  * Device: They are the hardware (different from sensors) of the desk 
  * Person: is the user 
  * PersonActivity: The user activities recognized by the desk based on specific conditions codded in SWRL
  * Sensor: A set of sensors 

![image](https://user-images.githubusercontent.com/91313196/205524606-5062736b-6ab4-4b2c-a849-3e295b1579b7.png)
## Object Properties
 * isNotUsing: a Person is not using a Desk component 
 * deskSuggestsTo: a Desk deskSuggestsTo DeskSuggestion
 * hasDevice: a Desk hasDevice Device 
 * hasSensor: a Desk hasSensor Sensors
 * inMode: a Desk is inMood DeskFeatures 
 * isDeviceOf: a Device isDeviceOf a Desk or a Chair
 * isDoneByPerson: a PersonActivity isDoneByPerson Person
 * isSensorOf: a Sensor isSensorOf Desk 
 * isModeOf: DeskFeatures isModeOf a Desk
 * isUsedBy: Desk component is used by Person 
 * isUsing: a Person is using a Desk component 
 * personIsDoing: a Person is doing a PersonActivity 

![image](https://user-images.githubusercontent.com/91313196/205525087-76ce391b-155a-411e-86fd-41b3e8168af5.png)

## Data Properties 
 * deviceState: Represents either the Device is On or Off by an integer value (0 if off) and (1 if on)
 * hasFitnessData: Assigns an integer value “number of minutes” the person has been standing up or sitting down from the starting of the day The data is assumed to be collected from a smart watch 
 * hasLightLevel: Assigns a string to the Sensor_LDR (dark, soft or light)
 * hasSentence: Assigns the sentence said by the user to the voice_recognition sensor
 * hasTemperature: Assign the temperature of the room (integer) to the temperature sensor 
 * hasTime: Assigns a time (integer) to the Digital clock Device
 * sensorState: Represents either the Device is On or Off by an integer value (0 if off) and (1 if on)

![image](https://user-images.githubusercontent.com/91313196/205525180-f35ed120-fb79-4ee0-aa56-989a9fd3f895.png)

##SWRL rules 

![image](https://user-images.githubusercontent.com/91313196/205525190-59820b71-7c8d-4572-b299-499b9739e759.png)

    

  


