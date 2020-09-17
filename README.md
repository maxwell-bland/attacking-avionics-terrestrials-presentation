# qualifying-exam

Material and notes relating to a depth subject discussing the threat vector
differences between air and ground cyber-physical systems (CPS).

What are the similarities and differences in adversary models and attacks for
flying vehicles (e.g. aircraft and drones) vs terrestrial vehicles
(automobiles, trucks, unmanned rovers)?  To the extent possible, discuss past,
current and future trends. 

# Earth and Wind: Flying and Terrestrial Vehicles, Adversary Models and Attacks

First, definitions.

## What do we define as a vehicle?

A mobile machine, i.e. any object capable of coordinating itself in space
according to a set of inputs. 

Flying: a vehicle coordinating itself in the atmosphere.  Terrestrial: a
vehicle coordinating itself on the ground.

We will include all the immediate material in contact with the material as the
vehicle.  Thus, the safety of the passengers comes into the domain of the
safety of the vehicle.

## What do we define as an adversary?

All objects are considered inputs to the material reality of the vehicle.
Material realities may be considered as being or not being.  Adversaries are a
continuum of causal priors to oppositional material realities.  That is, they
are the cause behind some continuum of material oppositions to other states of
being.  Note that these oppositions (attacks) are states of being in
themselves.  Adversaries are also material themselves, and thus restricted.

For examples, an adversary can be the environment itself.  An adversary could
also be a hacker capable of hijacking control flow.

But which adversaries are we worried about?  Clearly, the wind is not a
legitimate adversary.  We worry about human actors.  We worry about manifest
realities in which the vehicle performs some action contrary to intention.  We
worry about human actors that are the causative basis for these realities.

With this in mind, let us consider what an adversary can do to a vehicle.

1) Change the vehicle's movement/actions. (Security) 2) Leak information
carried by the vehicle. (Confidentiality/Privacy) 3) Masquerade as the vehicle.
(Authenticity) 4) Change information carried by the vehicle. (Integrity)

There is also the notion of activity/passivity, that is, whether the adversary
actively provides input to the vehicle.

## What do we define as an attack?

An attack is the potential material consequence of the adversary.  For an
attack to be considered valid, we must percieve its oppositional material
reality.  The material of an attack can be abstract or real.  When abstract, it
is an organization of material signifiers parrallel to other material.  When
realized, it is occuring: for example, the radio signals as they take over an
aircraft.

From the horse's mouth: Federal  Information  Processing  Standards  (FIPS)
defines  a  threat  as “Any circumstance  or  event with the  potential to
adversely impact organizational operations (including mission, functions,
image,  or reputation), organizational assets, or individuals through an
information system via unauthorized access, destruction, disclosure,
modification of information, and/or denial of service.

- Access: simple unauthorized access (e.g. unauthorized access to FMS, or EFB)
- Misuse: unauthorized use of assets (e.g. unauthorized use of CMU, or onboard
  internet router)
- Disclosure:   unauthorized   and illicit   disclosure   of   information
  (e.g.   publishing   FMS   or   EFBcredentials or confidential data)
- Modification:  making  unauthorized  changes  to  an  asset  (e.g. modifying
  the  route  submitted  via ACARS,  or  modify  weather  data,  or Air Traffic
Control  (ATC)  Winds or Air Operations Center (AOC) Winds data)
- Denial of access: blocking  legitimate  users  from accessing assets  (e.g.
  consuming bandwidthand/orblocking MCDUlogonaccess to Air Route Traffic
Control Centers also known as ARTCC stations)

[cite][https://commons.erau.edu/cgi/viewcontent.cgi?article=1364&context=publication]

## The Differences Between Air/Ground CPS

The above definitons, while general, give an initial clear conception of
difference.  Notably, air ad ground CPS differ in their mechanisms for
mobility.  Thus, they differ in their sensing mechanisms as well as movement
mechanisms.

Issues of mobility give rise to other security complications.  One example
would be passenger airplanes.  Due to their cost and complexity, passengers on
these planes require tickets.  These ticketing mechanisms can be insecure.
These vectors present alternative dangers that are not generally present in
terrestrial vehicles.

The typical perspective on this issue would be that there really is no
difference.  This is because sensor differences are generally abstracted away.
For example [1][https://journals.sagepub.com/doi/pdf/10.1177/1548512915617252]
demonstrates hacking a Parrot AR.Drone, a quadcopter with a broadcasted 802.11
network for control.  Here, the primary "attack" is on the network, and has
nothing to do with the fact the device is a drone.  However, what is done with
the drone after this point is of interest.

It is clear that these two vectors are out of the scope of this analysis.  That
is, I will ignore issues not relating to the mechanism of the vehicle itself.
The material differences between aerial and terrestrial vehicles give rise to
domain-specific attacks.  So, what are the material differences between aerieal
and terrestrial vehicles?  Well, we can start by examining a few vehicles.

### Civilian Transport 

#### The Infrastructure of a Passenger Aircraft

Let's consider the material affects a human can have on the mechanism of a
passenger aircraft.  Well, they could change it's position in space.  At least
in this case, the plane does not really have other "functions".  So, let's see
how the position in space is controlled in a passenger aircraft.

Aircraft have evolved from using seperate electronic systems, to seperate
interconnected systems, to fully integrated systes.  Seperated interconnected
systems are termed "federated" avionics.  Fully integrated systems are
"modular" avionics.  Federated avionics are used in the most common passenger
aircraft today, including the Boeing 737.
[4][https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=4106349]

Federated aircraft operate via the communication of several Line Replacable
Units (LRUs).  [3][https://www.usenix.org/system/files/cset19-paper_crow.pdf]
It is assumed in this case that these LRUs contain no sensitive information.
This assumption is broken under obvious cases.  It is also assumed they are
airgapped from passenger network traffic.  This assumption would be broken in
the case of some malicious, attached device broadcasting wifi into the cabin.

Another note: it is possible to buy LRUs online (from personal experience).  We
can assume any adversary has access to the code running on the plane.

For simplicity, let's limit the adversary to someone who does not want to take
over the cockpit in-flight.  The justification for this is that we already have
checks (unrelated to the vehicle's mechanism).  Though this assumption can be
broken as well, for example, with the Germanwings  flight  allegedly  crashed
by  a  suicidal pilot.
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]

That limits us to two options: either remote takeover "in-the-sky" or prior to
this, "on-the-ground".  Despite my mention of Line Replaceable Units, from the
"philosophy" above, ANYTHING that could effect the position or function of the
vehicle's mechanism is fair game.

It includes, for example, the fueling carts which are used to provide gas to
the airplane before flight.  These operate via computers, and could change the
amount of fuel provided.  Clearly these systems, or the multitude of air
traffic control systems used for flight planning are far outside the scope of a
20 minute discussion.  However, I would like to note that in 2015, LOT Polish
Airlines was forced to ground flights at Warsaw airport afterhackers disabled
the flight plans for outbound air-craft.
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]

Thus, confining further, let us refine our model to the material that is/will
be present when the aircraft is in the air.  We still have attacks either
remotely or via prior-on-the-ground.  Since remote takeover is more spicy, we
can start with that.

There are several Radio Frequency (RF) links present on the aircraft, each of
which is potentially dangerous.  These include the radio altimeter, used to
determine the height of the aircraft, the Doppler NAV at 8.8 Ghz, VHF NAV and
comm links for determining flight information, and others.  There also exist
connections via the Global Navigation Satellite System or the Automatic
Dependent Surveillance Broadcase (ADS-B).  ADS-B, for example, provides
information on traffic, weather, and flight information.
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]
Note that, ADS-B, for example, is unencrypted, and thus liable to spoofing.
[cite][https://www.securityweek.com/air-traffic-control-systems-vulnerabilities-could-make-unfriendly-skies-black-hat]

These connections are, for example, forwarded into a system for communication.
In the case of federated avionics, like the 737 (and at least 10 other
aircraft), this is a Communication Management Unit (CMU).  This single computer
consisting of a set of several processors for different tasks, is the "gateway"
to the rest of the aircraft.  It serves as the primary attack surface (though
technically there are systems before this fielding RF signals directly).

From this, the attack surface diverges in the case of federated systems.  There
would be several options for attack, including cockpit display units or the
flight management computer directly.  Unlike simpler systems, each of these
LRUs typically runs its own Real-Time OS (RTOS), and has several applications
running.  They communicate via the ARINC standard set.

In the case of Integrated Modular Avionics, there is an IMA platform that
defines the allocation of functions for the aircraft.  Bythis, understand that
communications and I/O are hared across several processors, which are logically
delegated to tasks.  Little has been done in the study of IMA platform
security.  However, it is likely that the IMA logic for a 777 includes a
function for fielding, for example ACARS messages.  The code for this function
would be the target of any adversary.
[cite][https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=4106349]

In any case, even though there are a number of computer systems on the
aircraft, there are a number of manual overrides, and the adversary would still
need to "fool" the human pilots.  The extent to which this is possible has been
unstudied.

Clearly regardless of the RF channel used, the attack is classic: get control
over the system, leak some information from the system, etc..  The more
interesting problems come in the analysis of these systems and the programming
of path diversion, or human-factors analysis to cause the pilots to make the
incorrect moves.  Of course, addressing each possible computation that, for
instance, the flight management computer does in adjusting for wind speed, is
beyond the scope of this presentation.

That brings us to on the ground attacks.  Clearly, the attacker could try to
change the software running on an LRU by updating it, if access is possible.
They could also physically damage some components, or add some sort of implant
to the plane, which allowed for control mid-flight.  This is as much as I can
say on this topic.

#### The Infrastructure of a Passenger Car

The attack motive with a passenger car is similar to that of a transport aircraft.
The adversary motive is to change the car's position in space.
However, unlike passenger aircraft, there is actually sensitive data on some ECMs.
Notably, engine calibration information, which can be used by competitors to 
exfiltrate tuning information.
This information, once known, can actually be worth several thousand to
hundreds of thousands of dollars (from experience). 

Almost reminescent of a federated aircraft, passenger cars operate through a
series of Electronic Control Units.  Many modern consumer automobiles
coordinate between ECUs via the Controller Area Network (CAN) bus protocol,
though older cars and some marine vehicles, use protocols such as General
Motor's ALDL. 

We also, once again, may seperate the vehicle from the environment: several
teams have hacked traffic light, surviellance camera systems, and automotive
"infrastructure". [cite][https://jhalderm.com/pub/papers/traffic-woot14.pdf]
Yours truly worked on the problem of skimming at gas stations. 

We then also have the seperation of prior to driving vs. during-drive attacks.
Of course, the classic paper by Checkoway et al.
[cite][https://www.usenix.org/legacy/event/sec11/tech/full_papers/Checkoway.pdf]
demonstrated the RF attack surface of automotive computers, or Roufet  al.’s
recent  analysis  of  the  wireless  Tire Pressure Monitoring System (TPMS) in
a modern vehicles.
[cite][https://www.usenix.org/legacy/events/sec10/tech/full_papers/Rouf.pdf]
There are a plethora of long-range wireless and short-range wireless attacks
on passenger cars:  
From Checkoway et al.
"Global PositioningSystem (GPS),3Satellite Radio (e.g., SiriusXM
receiverscommon to late-model vehicles from Honda/Accura, GM,Toyota, Saab,
Ford, Kia, BMW and Audi), Digital Radio(including the U.S. HD Radio system,
standard on 2011Ford and Volvo models, and Europe’s DAB offered inFord, Audi,
Mercedes, Volvo and Toyota among others),and the Radio Data System (RDS) and
Traffic MessageChannel (TMC) signals transmitted as digital subcarrierson
existing FM-bands"

Of course, the key difference with this RF attack surface and passenger
aircraft is that it includes short-range RF signals such as Bluetooth and
Remote Keyless Entry.

There is still the matter of, once the ECU responsible for fielding the RF communication 
is breached, a seperate attack must be made on the ECM (Engine Control Module) in order
to change the fuel injection patterns, or on the ECU controlling the breaking system. 
The attack is dependent upon the adversary's goals.

Again, there is also the matter of human factors: although not present in all consumer 
automobiles, the goal (such as murder) may not be possible simply by crashing the automobile
into a wall.

On the ground attacks are also remarkably similar to aircraft, though perhaps less complex.
i.e. you can cut someone's break lines.

Moving into the future, we have systems such as the Tesla autopilot, additional algorithms that
can be attacked, perhaps due to additional inputs.
Ignored occlusion patterns in LiDAR point clouds make self-driving cars
vul-nerable to spoofing attacks [cite][https://www.usenix.org/system/files/sec20-sun.pdf].
Clearly, a passenger airplane may use LiDAR, but this seems less likely than a self-driving car.

### Military Use 

Until this point, we have assumed that the function, action of the vehicle in
question has been entirely movement in space, however, this is restrictive. The
question becomes, what of the attack surfaces of a vehicle designed for a
particular task, such as surveillance, offense (missiles, bombs), and defensive
mechanisms (avoidance of missles).

#### The Infrastructure of a General Atomics MQ-1 Predator Drone

Modified and upgraded to carry and fire two AGM-114 Hellfire missiles or other
munitions.  Retired in 2018.  Also can be used for surveillance.  Thus, the
information carried by the drone may be sensitive, revealing key locations it
has taken photos of.  Note that all movement of the drone is controlled via
long-range RF.  Thus, there are fewer human factors involved in malicious
takeover.  Controlled "via a C-band line-of-sight data link or a Ku-band
satellite data link for beyond-line-of-sight operations" (wikipedia).  Radio is
an ARC-210, with built in anti-jamming capabilities, including Havequick and
SINCGARS.  These systems operate via a set of sophisticated frequency hopping
and anti-jamming algorithms.
[cite][https://www.af.mil/About-Us/Fact-Sheets/Display/Article/104469/mq-1b-predator/]
There are other components responsible for flight, but it is key to understand
that connections are encrypted.  Uses CTCSS, Continuous Tone-Coded Squelch
System, which encodes a low-frequency tone into the signal so only the intended
signals are heard on a noisy channel.
[cite][https://web.archive.org/web/20160304081715/http://www.afceaboston.com/documents/events/cnsatm2011/Briefs/02-Tuesday/Tuesday-PM%20Track-2/04-Maher-ARC-210%20Program%20Overview-Tuesday%20Track2.pdf]
[cite][https://www.raytheon.com/capabilities/products/apx100v] Still, the
ARC-210 is manufactured by Rockwell Collins, so one adversary model is a
manufacture-time attack, reasonable in the case of national adversaries.
Still, an adversary process would be the same: there are a unique set of
protocols used by the ARC-210, such as the Tactical Secure Voice Cryptographic
Interoperability Specification (TSVCIS) and MIL-STD-188, the military standard
for telecommunications.  The main differences are that 1) acquiring components
is more difficult, and 2) the protocols and systems are harder to attack.  An
adversary would also need to compromise mission-specific RF control keys, so
long as there are not vulnerabilities in message reciept functions.
[cite][https://apps.dtic.mil/dtic/tr/fulltext/u2/a538348.pdf] also outlines
potential attacks that can occur by requiring high precision control of the
MQ-1 predator.  i.e. certain ground-to-air missile tracking methods may be
capable of taking down a drone due to the capacity of the system for piloting
under fine-grained scenarios.  This is partially due to the human factors
involved in piloting the drone.

#### The Infrastructure of a Tank

### Civilian Use 

#### The Infrastructure of a Drone 

#### The Infrastructure of a Rover

Example: "White  Sands  Missile  Range  test  exercise  demon-strated that the
GPS signals used for navigating anunmanned  aircraft,  or  drone,  can  be
accessedremotely to divert the flight onto erroneous paths." Example:
"Germanwings  flight  allegedly  crashed  by  a  suicidal pilot"
[2][https://commons.erau.edu/cgi/viewcontent.cgi?referer=https://scholar.google.com/&httpsredir=1&article=1343&context=publication]



Aircraft, drones have greater degrees of mobility in their route planning. 

They may also deal with mobility-based defense mechanisms, i.e. dodging
missiles.  To an extent, terrestrial vehicles may also need to dodge threats.

Crucially, the greater degree of mobility is one categorical dissimilarity
between air and terrestrial vehicles.

## The Similarities Between Air/Ground CPS

Consider that both air and ground CPS are "machines" with material outputs,
inputs.  Consider that in both cases there are tight environmental timing
constraints.  Consider that both air and ground CPS will use programmable
microcontrollers, embedded RTS.  Potentially entire operating systems: at the
end of the day, these are computers.

## Historical Context

Unmanned Autonomous Vehicles (UAVs) have gained traction.  False Data Injection
(FDI) attacks the null space of CPS matrix computations.  FDI circumvents error
detection techniques in sensor technologies.

Artificial neural network technologies can detect abnormal fluctuations in
sensor values.

Work in the domain of mobile systems is ultimately work in non-mobile systems.
E.g. my work on analyzing the update mechanisms for aircraft, other work on EV
power stations.

Programmable Logic Controllers (PLCs) 

## The Current State

## Potentialities

"Proactively addressing security threats to the mostsafety-critical  systems
requires  the  expertise  of  theuser  community—air  traffic  controllers,
mainte-nance  technicians,  pilots,  and  security  experts—toidentify and rate
the potential risks and to focus themitigation  options  on  the  most critical
issues."

## References


