

## Background
Todays computing devices cannot be independently verified, and thus not trusted.
The devices are incredibly complex, and their software stack similarly so.
A modern mobile device or laptop/desktop computers have many processing units,
all with propriatary embedded firmware/microcode.
Many of the processors have direct (or poorly mediated) access to system memory, central processing units
and network devices.


The expected richness of computing applications also requires quite powerful devices.

Perhaps we can use blockchain-like trustless computing in order to offload most computations
from the individual devices, so that only a (relatively) thin client is needed.

If one could massively reduce the local computations required, this might simplify the
job of creating a first fully trustable personal computing device. Open source and independently verifiable.

If able to bring such a device to a minimally useful state, the project may act as a beachhead,
opening up for more complex follow-up projects.


How to avoid that such project is only used by 'those with special privacy interests',
and thus be considered a surveillance target merely for using the platform?
And it being hard to acheive the scale required for

Bitcoin mining used potential of direct economic gain to acheive scale.

## Trustless 'cloud computing'

Run remote jobs on multiple pieces of hardware, in different infrastructures, verify their outputs against eachother.
This is general-computing

How to let workers do work, without knowing who it is for?
How to let workers do work on private data?


## Trusted thin client

Design with long-term goal of self-fabbing.
Intermediate goal of having testbenches for verifying components.
White-box: xray/electronmicroscopy
Black-box: functional tests

How to avoid open-source nature of the tests allowing attacked to reproduce the tests, and thus designing for them?
Re-test devices with updated/changed benches after production?
Testing sites then become targets for attack

Communication
Productivity

Web browser
Email
SSH terminal

Computation unit w/memories.
Display. LCD, OLED/AMOLED, eINK?
Input devices. Keyboard+touchscreen/pad.
Network devices.

end-to-end cryptography, compression/decompression

How to decide what kind of off-the-shelf components are acceptable?
Establish a kind of DMZ for non-trusted components, which cannot affect general computation,
and treat input as untrusted.
The better/more we can do this, the less things we have to re-invent, reducing burden to get to minimally useful state. 

Can we safely operate over commodity untrusted networks?
end2end crypto should ensure data authenticity, but network usage may require compromisable programmability.

Issue with untrusted network device though, is not so much about ability to compromise data,
but also it leaking information without control. Either info that helps indentifying/fingerprinting,
or sensor or location data.

