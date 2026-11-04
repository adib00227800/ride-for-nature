# Ride For Nature — Spoke-Driven Bicycle Charger

A compact mechanism that mounts on a bicycle wheel hub and converts the wheel's rotation into electricity to charge a power bank or phone on long rides.

![Gear train](images/gear_train.png)

## Problem

Cyclists on long routes have no convenient way to keep a phone or power bank charged. The common solutions each fall short:

- **Friction (bottle) dynamo:** weak output.
- **Hub dynamo:** expensive.

Goal: a low-cost, easy-to-install unit that generates useful power from an ordinary bicycle wheel.

## Constraints

- Installs easily on an ordinary bicycle wheel
- Fits within the wheel's available space
- Low cost; manufacturable by 3D printing

## Concept

The unit mounts on the wheel hub: a central bore fits around the hub axle and holds the housing stationary. The large drive gear carries several protrusions that engage the wheel's metal spokes, so the spinning wheel turns the gear while the housing stays fixed. A compound gear train steps the speed up 5×, driving a small DC generator, and a charging circuit conditions the output to USB.

![Mounted on the wheel](images/mounted_on_wheel.png)

▶ **Installation video:** [media/install.mp4](media/install.mp4)

## Key engineering decisions

**Torque to speed.** Wheel speed is far below the speed a generator needs, so the mechanism trades the wheel's torque for rotation speed through a compound gear train. The ratio was pushed as high as space allowed (1:5); a higher ratio would have made the unit too large to fit within the wheel.

**Drive through the spokes.** Taking the drive from the spokes via protrusions on the large gear leaves the wheel itself unmodified and makes installation quick.

**Packaging.** The size envelope inside the wheel was the main limit on the gear ratio, so the housing is compact and curved, with the electronics in a separate pocket beside the gear train.

**Design for manufacture.** Housing, gears and bearing seats were designed with component-design principles for 3D printing; every shaft runs on bearings.

## Design

| CAD (closed) | CAD (gear train) |
|---|---|
| ![](images/cad_housing_closed.png) | ![](images/cad_gear_train.png) |

Housing drawing: [cad/housing_drawing.png](cad/housing_drawing.png)

| Item | Value |
|---|---|
| Overall housing size | approx. 134 × 131 × 76 mm |
| Gear ratio | 1 : 5 (speed-up) |
| Housing / gear material | PLA, FDM 3D-printed |
| Mounting | Wheel hub; driven through the spokes |

## Build and test

- Designed in SolidWorks; printed in PLA
- Built and wired the charging circuit; it worked as intended
- Mounted the prototype on a bicycle wheel
- Charged a phone while the wheel was turned by hand

![Phone charging during test](images/phone_charging_test.png)

![Assembled housing](images/housing_closed.png)

## Results and limitations

- The concept works: the mechanism mounts easily and generates power.
- An off-the-shelf DC motor and capacitors stood in for a purpose-built mini generator, so this is a proof of concept, not a product.
- Output was not measured.
- Not road-tested: the housing walls were too thin for riding loads.

## Next steps

- Thicker or reinforced housing, or a stronger material (PETG, nylon)
- Replace the DC motor with a proper mini generator
- Measure power output against wheel speed

## Team

Adib Saffarifard and Soheil Dehghani Firouzabadi, supervised by Dr. Mohsen Hamedi, Amirkabir University of Technology, 2025. All work was done jointly.
