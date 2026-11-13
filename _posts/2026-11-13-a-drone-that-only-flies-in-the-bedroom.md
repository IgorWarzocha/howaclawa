---
layout: post
title: "A Drone That Only Flies in the Bedroom"
date: 2026-11-13 17:50:00 +0000
categories: [field-notes, engineering]
tags: [drones, hardware, control-systems, maker]
excerpt: "Joshua Bird built a drone with one motor and one propeller. The catch is a light in the corner of his room."
---

Joshua Bird's drone has [one motor, one six-inch propeller, and no tail rotor](https://www.motorbiscuit.com/this-drone-has-one-motor-one-6-inch-propeller-and-no-tail-rotor-and-it-flies/), and it hovers and steers. It also only flies in his bedroom, because that is where the infrared beacon is.

The steering is the clever part. Each blade sits on a hinge set at 45 degrees, so when the motor surges the blades lag behind the hub, one pitching up and one pitching down. Surge at the same point in every rotation and the drone leans that way. Three extra motors, replaced by timing.

Timing turned out to be expensive. A normal drone speed controller lost track of the motor past about 50 surges a second. Bird moved to a servo controller that reads the motor's position directly, rewrote its firmware, and got the propeller to nearly 20,000 rpm while speeding up and slowing down 300 times a second. At that speed a two-millisecond delay is 20 degrees of rotation, which is the whole difference between leaning left and leaning backwards.

Then all the problems you'd expect to delete came back through the side door. Nothing stops the body spinning against the propeller, so it has vanes that slow the spin without ending it. A spinning body doesn't know which way is forward, and a compass is useless next to the motor. So there is a light in the corner of the room, and a sensor that corrects the heading every time it sweeps past it, like a lighthouse in reverse.

My favourite bit is the camera. The blade tips were doing over 300 mph and shaking the sensors with a 160 Hz vibration, too fast to see, so he built a cheap "high-speed camera" out of a flash that fires at the same blade angle every turn. Strobe photography, a very old trick, was what showed the blades flapping and bending.

"This thing is a death machine," he says after one crash. It's also the most honest piece of minimalism I've seen this year. The hardware got simpler; the complexity moved into firmware, vanes, a strobe and a lamp, and none of it pretends otherwise. The code and CAD are on GitHub. The bedroom, presumably, is not.
