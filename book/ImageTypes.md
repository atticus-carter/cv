(lesson-1)=
# Introduction to Ocean Image Data

## Overview

In this lesson, we will explore **marine photographic and videographic data**. We will also discuss the tools used to capture these images and videos, such as **underwater cameras**, **drones**, and **satellite imagery**. Understanding this data is the first step toward applying **Computer Vision (CV)** techniques to oceanographic research.

### Learning Objectives

By the end of this section, you will:
- Understand the different types of ocean image data.
- Identify the tools and techniques used to capture marine imagery.
- Learn how CV can be applied to oceanographic research.

---

## Types and Tools for Capturing Ocean Image Data

Ocean image data comes from a variety of sources, each with unique strengths and limitations. Let's explore the main types of ocean image data and the tools used to capture them.

### Underwater Imagery

Underwater imagery is captured using technologies like **Remotely Operated Vehicles (ROVs)**, **Autonomous Underwater Vehicles (AUVs)**, and **fixed underwater cameras**.

#### ROVs (Remotely Operated Vehicles)

ROVs are uncrewed submersibles controlled from the surface. They provide real-time video and still imagery, often equipped with sampling tools. Notable examples are:

- **Jason**: Capable of deep-sea exploration, reaching depths of up to 6,500 meters. Operated by WHOI, it includes high-definition video and robotic arms for sample collection.
- **ROPOS**: A Canadian ROV capable of diving to depths of 5,000 meters, ideal for exploring hydrothermal vent systems.

:::{figure} images/image-1.png
:name: rov-jason
The ROV Jason Equipped with 4k video cameras. Credit: M. Elend, University of Washington
:::

**Advantages of ROVs**:
- Real-time control for targeted exploration.
- Deep-water capabilities beyond the reach of divers.

**Drawbacks of ROVs**:
- High cost and limited mobility due to tethers.

#### AUVs (Autonomous Underwater Vehicles)

AUVs are pre-programmed to follow missions autonomously, capturing imagery without human intervention. A prime example is **Sentry**, which collects data at depths of up to 6,000 meters.

:::{figure} images/image-3.png
:name: auv-sentry
AUV Sentry at the surface after a deep dive. Credit: WHOI
:::

**Advantages of AUVs**:
- Autonomous, covering large areas efficiently.
- Can be fitted with multiple sensors.

**Drawbacks of AUVs**:
- Limited real-time control and operational time due to battery life.

#### Fixed Underwater Cameras

These cameras are positioned on the seafloor for long-term monitoring. The **Ocean Observatories Initiative's Regional Cabled Array** provides live video feeds from deep-sea environments.

:::{figure} images/image.png
:name: underwater-camera
A digital still camera capturing methane seep activity. Credit: UW/NSF-OOI/WHOI
:::

**Advantages of Fixed Cameras**:
- Ideal for long-term ecological studies.
- High-definition video and still imagery.

**Drawbacks of Fixed Cameras**:
- Limited to specific, small areas.

### Satellite Imagery

Satellites offer broad coverage for observing large-scale oceanographic phenomena, such as **phytoplankton blooms** and **sea surface temperature**.

:::{figure} images/image-2.png
:name: satellite-imagery
Satellite imagery showing a phytoplankton bloom. Credit: NASA Goddard Space Flight Center, Ocean Ecology Laboratory
:::

**Advantages of Satellite Imagery**:
- Global coverage and ability to monitor seasonal changes.
  
**Drawbacks of Satellite Imagery**:
- Lower resolution compared to underwater systems, making it less ideal for studying small-scale features.

### Aerial Imagery

Aerially mounted cameras on drones, planes and helicopters can produce high quality often georeferenced imagery of nearshore sites or areas that are hard to get to by other means of transport like sea ice.

:::{figure} images/image-4.png
:name: seal-population
Seals on Arctic sea ice captured with an aerial camera, annotated with a CV model. Credit: A. Carter, NOAA National Marine Mammal Laboratory
:::

**Advantages of Aerial Imagery**:
- Large georeferenced imagery can be obtained in relatively quick transects.
  
**Drawbacks of Aerial Imagery**:
- Aerial imagery doesn't capture underwater information, and can be very expensive to operate.
