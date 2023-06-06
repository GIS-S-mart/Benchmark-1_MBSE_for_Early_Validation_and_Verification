# WONKA Case Study


## Description

The WONKA case study comprehends five systems in their respective environments, for which a scientific approach is designed to fulfill dedicated specifications. The system "to design" is the scientific approach to be validated, hereinafter denoted ATV.

**GOAL**: verify and validate a scientific approach on two industrial systems, given three laboratory systems. The solution shall enable systems engineer to correct, complete and verify specifications as early as possible (before/after experiments on laboratory systems, before/after experiments on industrial systems), taking into account the limited availability and cost of experiments on industrial systems.

The use cases, scientific approach and ontology making up this case study are presented below. The ontology provides a framework to formally represent the constitutive elements of this case study.

---
#### <u> Use cases </u>

##### Three *laboratory systems*:

1. Coffee Machine

The Coffee Machine use case consists of 1 automatic coffee machine (1 heating coil, 1 grinder, 1 pump and 1 moving infuser) and 8 sensors (3 accelerometers, 2 temperature sensors, 1 laser distance sensor, 1 current sensor, 1 voltage sensor).

<figure class="image">
  <img src="fig/coffeemachine.png" width=400>
  <figcaption><b>Figure 1: Laboratory instrumented coffee machine.</b></figcaption>
</figure>

1. Robot Arm

The 6-axis robot arm repeatedly performs a specific motion (e.g., piece-picking). It consists of 6 (electrical) brushless motors to put each axis in motion, and it is equipped with 1 accelerometer to sense the motors' vibrations.

<figure class="image">
  <img src="fig/ur10-robot.png" width=400>
  <figcaption><b>Figure 2: Laboratory instrumented 6-axis robot arm.</b></figcaption>
</figure>

3. 3D Printer

A laboratory Cartesian Fused Deposition Modelling (FDM) 3D printer is considered. The printer repeatedly manufactures a specific part. It consists of 4 (electrical) stepper motors moving the extruder along 3 directions and pushing the filament forward to be fused, together with 2 heating resistors (one for the bed, one on the extruder). The 3D printer is equipped with a single current sensor.

<figure class="image">
  <img src="fig/3dprinter.png" width=400>
  <figcaption><b>Figure 3: Laboratory instrumented  cartesian fused deposition modelling (FDM) 3D printer.</b></figcaption>
</figure>

##### Two *industrial systems* (from the [EnerMan Project](https://enerman-h2020.eu/)):

4. Temperature-Controlled Vehicle Testbed

The temperature- and humidity-controlled vehicle testbed is composed of 2 independent heating, ventilation and air conditioning (HVAC) systems. Overall, there are 2 cooling coils, 1 heating coils, 1 fan, 1 humidifier and 1 dehumidifier. The room is instrumented with 2 temperature sensors (1 after the first HVAC, 1 in the chamber).
In this use case, the only objective is to decompose the temperature signals.

<figure class="image">
  <img src="fig/vehicle_testbed.png" width=400>
  <figcaption><b>Figure 4: Temperature- and humidity-controlled chamber of a vehicle testbed.</b></figcaption>
</figure>

5. Mixing and Conching Machine in a Chocolate Factory

The mixing and conching machine is responsible for stirring and heating up chocolate within a chocolate factory. The machine consists of 1 (electrical) three-phase alternative current motor and 1 heating coil. The heating mechanism is assumed to be electrically powered. The machine is instrumented with 3 current sensors (one on each phase of the current supply).

<figure class="image">
  <img src="fig/chocolatefactory.png" width=400>
  <figcaption><b>Figure 5: Mixing and conching machine heating up and stirring chocolate.</b></figcaption>
</figure>

---
#### <u> Scientific approach </u>

The scientific approach consists in a *Blind Source Separation* problem. That is, one seeks the activation sequence of each actuator within a system in an unsupervised fashion, i.e., exclusively from sensor data.

<figure class="image">
  <img src="fig/blindsourceseparation.png" width=500>
  <figcaption><b>Figure 6: Illustration of the activation sequence synthesis problem.</b></figcaption>
</figure>

---
#### <u> Ontology </u>

In order to compare heterogeneous systems with one another, the [SAREF](https://saref.etsi.org/core/v3.1.1/) ontology (and [SAREF4INMA](https://saref.etsi.org/saref4inma/v1.1.2/) module) has been refined into the [wonka](ontology/raw/wonka.owl) ontology. This ontology can be visualised using [WebVOWL](https://service.tib.eu/webvowl/) (simply import the `.owl` file). 

The use cases have been formally represented in this ontology using the following implementation blueprint:

<figure class="image">
  <img src="fig/ontology_blueprint.png" width=500>
  <figcaption><b>Figure 7: Implementation blueprint of the knowledge base.</b></figcaption>
</figure>

Once instantiated, the ontology can be visualised as a knowledge graph:

<figure class="image">
  <img src="fig/knowledgegraph.png" width=500>
  <figcaption><b>Figure 8: Knowledge graph for the WONKA dataset.</b></figcaption>
</figure>


## Initial requirements

#### <u> Requirements </u>

The requirements can be categorised as *dynamic* if its compliance requires an experiment on a system, or *static* otherwise. The initial requirements are as follows:

| Requirement | Desrcription / Related question for query |
|---|---|
| Req 2.1<br>(dynamic) | Does the ATV accurately estimate the<br>sequence of operating modes, given a<br>performance threshold? |
| Req 2.2<br>(dynamic) | Does the ATV accurately identify the<br>actuators activated in each operating mode? |
| Req 4.3<br>(static) | What are the elements of the environment<br>that may tamper with the results of the ATV? |

<!-- 
| Req 2.7<br>(static) | For each actuator within a system of interest,<br>is there at least one sensor monitoring an<br>observable property this actuator affects? |

| Req 2.9<br>(static) | In a sensor energy domain, are the actuator-originated signals <br>coupled with one another? (i.e., actuators in series association) |

| Req 3.15<br>(static) | Does each sensor have a sampling rate <br>at least twice the maximum frequency of <br>the signals the actuators it monitors can produce? | 
-->


The requirements formally expressed as SPARQL queries can be found [here](requirements_as_sparql_queries/).