# qualifying-exam

Material and notes relating to a depth subject discussing the threat vector
differences between air and ground cyber-physical systems (CPS).

What are the similarities and differences in adversary models and attacks for
flying vehicles (e.g. aircraft and drones) vs terrestrial vehicles
(automobiles, trucks, unmanned rovers)? 
To the extent possible, discuss past, current and future trends. 

# Earth and Wind: Flying and Terrestrial Vehicles, Adversary Models and Attacks

First, definitions.

## What do we define as a vehicle?

A mobile machine, i.e. any object capable of coordinating itself in space according to a set of inputs. 

Flying: a vehicle coordinating itself in the atmosphere. 
Terrestrial: a vehicle coordinating itself on the ground.

We will include all the immediate material in contact with the material as the vehicle.
Thus, the safety of the passengers comes into the domain of the safety of the vehicle.

## What do we define as an adversary?

All objects are considered inputs to the material reality of the vehicle.
Material realities may be considered as being or not being.
Adversaries are a continuum of causal priors to oppositional material realities.
That is, they are the cause behind some continuum of material oppositions to other states of being.
Note that these oppositions (attacks) are states of being in themselves.
Adversaries are also material themselves, and thus restricted.

For examples, an adversary can be the environment itself.
An adversary could also be a hacker capable of hijacking control flow.

But which adversaries are we worried about? 
Clearly, the wind is not a legitimate adversary. 
We worry about human actors.
We worry about manifest realities in which the vehicle performs some action contrary to intention.
We worry about human actors that are the causative basis for these realities.

With this in mind, let us consider what an adversary can do to a vehicle.

1) Change the vehicle's movement/actions. (Security)
2) Leak information carried by the vehicle. (Confidentiality/Privacy)
3) Masquerade as the vehicle. (Authenticity)
4) Change information carried by the vehicle. (Integrity)

There is also the notion of activity/passivity, that is, whether the adversary
actively provides input to the vehicle.

## What do we define as an attack?

An attack is the potential material consequence of the adversary.
For an attack to be considered valid, we must percieve its oppositional material reality.
The material of an attack can be abstract or real. 
When abstract, it is an organization of material signifiers parrallel to other material. 
When realized, it is occuring: for example, the radio signals as they take over an aircraft.

## The Differences Between Air/Ground CPS

The above definitons, while general, give an initial clear conception of difference.
Notably, air ad ground CPS differ in their mechanisms for mobility.
Thus, they differ in their sensing mechanisms as well as movement mechanisms.

Issues of mobility give rise to other security complications.
One example would be passenger airplanes. 
Due to their cost and complexity, passengers on these planes require tickets.
These ticketing mechanisms can be insecure. 
These vectors present alternative dangers that are not generally present in terrestrial vehicles.

The typical perspective on this issue would be that there really is no difference.
This is because sensor differences are generally abstracted away. 
For example [1][https://journals.sagepub.com/doi/pdf/10.1177/1548512915617252] demonstrates hacking 
a Parrot AR.Drone, a quadcopter with a broadcasted 802.11 network for control. 
Here, the primary "attack" is on the network, and has nothing to do with the fact the device is a drone.
However, what is done with the drone after this point is of interest.

It is clear that these two vectors are out of the scope of this analysis.
That is, I will ignore issues not relating to the mechanism of the vehicle itself.
The material differences between aerial and terrestrial vehicles give rise to domain-specific attacks.
So, what are the material differences between aerieal and terrestrial vehicles?
Well, we can start by examining a few vehicles.

### Civilian Transport 
#### The Infrastructure of a Passenger Aircraft

Let's consider the material affects a human can have on the mechanism of a passenger aircraft.
Well, they could change it's position in space.
At least in this case, the plane does not really have other "functions".
So, let's see how the position in space is controlled in a passenger aircraft.

Passenger aircraft operate via the communication of several Line Replacable Units (LRUs).
It is assumed in this case that these LRUs contain no sensitive information.
This assumption is broken under obvious cases. 
It is also assumed they are airgapped from passenger network traffic.
This assumption would be broken in the case of some malicious, attached device broadcasting wifi into the cabin.

Another note: it is possible to buy LRUs online (from personal experience). 
We can assume any adversary has access to the code running on the plane.

For simplicity, let's limit the adversary to someone who does not want to take over the cockpit in-flight.
The justification for this is that we already have checks (unrelated to the vehicle's mechanism).
Though this assumption can be broken as well, for example, with the Germanwings  flight  allegedly  crashed  by  a  suicidal pilot.
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]

That limits us to two options: either remote takeover "in-the-sky" or prior to this, "on-the-ground".
Despite my mention of Line Replaceable Units, from the "philosophy" above, ANYTHING that could effect the position or function of the vehicle's mechanism is fair game.

It includes, for example, the fueling carts which are used to provide gas to the airplane before flight.
These operate via computers, and could change the amount of fuel provided.
Clearly these systems, or the multitude of air traffic control systems used for flight planning are far outside the scope of a 20 minute discussion.
However, I would like to note that in 2015, LOT Polish Airlines was forced to ground flights at Warsaw airport afterhackers disabled the flight plans for outbound air-craft.
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]

Thus, confining further, let us refine our model to the material that is/will be present when the aircraft is in the air.
We still have effects either remotely or via a prior on-the-ground attack.

Since remote takeover is more spicy, we can start with that:

" Radio frequency(RF)  links  into  the  aircraft  may  provide  a  possiblepoint  of  entry  for  the  introduction  of  malwareattacks. Many of these links—but not all—are con-sidered strong and robust and may limit the oppor-tunity to jam or spoof the signals without detection.  Weak RF links in the system include the GlobalNavigation Satellite System signal that provides crit-ical navigation information to the pilot and transmitsdata  to  air  traffic  controllers  via  an  onboard  Auto-matic  Dependent  Surveillance–Broadcast  (ADS-B).An   independent   validation   process   has   beendesigned  to  address  some  of  the  threats  to  thesedata—secondary  means  are  needed  to  validate  theaircraft’s location.  "
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]

#### The Infrastructure of a Passenger Car

### Military Use
#### The Infrastructure of an Unmanned Aerial Vehicle (UAV)
#### The Infrastructure of a Tank

### Civilian Use
#### The Infrastructure of a Drone
#### The Infrastructure of a Rover

Example: "White  Sands  Missile  Range  test  exercise  demon-strated that the GPS signals used for navigating anunmanned  aircraft,  or  drone,  can  be  accessedremotely to divert the flight onto erroneous paths."
Example: "Germanwings  flight  allegedly  crashed  by  a  suicidal pilot"
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]



Aircraft, drones have greater degrees of mobility in their route planning. 

They may also deal with mobility-based defense mechanisms, i.e. dodging missiles.
To an extent, terrestrial vehicles may also need to dodge threats.

Crucially, the greater degree of mobility is one categorical dissimilarity between air and terrestrial vehicles.

## The Similarities Between Air/Ground CPS

Consider that both air and ground CPS are "machines" with material outputs, inputs.
Consider that in both cases there are tight environmental timing constraints.
Consider that both air and ground CPS will use programmable microcontrollers, embedded RTS.
Potentially entire operating systems: at the end of the day, these are computers.

## Historical Context

Unmanned Autonomous Vehicles (UAVs) have gained traction.
False Data Injection (FDI) attacks the null space of CPS matrix computations. 
FDI circumvents error detection techniques in sensor technologies.

Artificial neural network technologies can detect abnormal fluctuations in sensor values.

Work in the domain of mobile systems is ultimately work in non-mobile systems. 
E.g. my work on analyzing the update mechanisms for aircraft, other work on EV power stations.

Programmable Logic Controllers (PLCs) 

## The Current State

## Potentialities

"Proactively addressing security threats to the mostsafety-critical  systems
requires  the  expertise  of  theuser  community—air  traffic  controllers,
mainte-nance  technicians,  pilots,  and  security  experts—toidentify and rate
the potential risks and to focus themitigation  options  on  the  most
critical  issues."

## References


