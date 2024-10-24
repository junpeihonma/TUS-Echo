# TUS-Echo

TUS-ECHO: COLLECTION OF REAL ECHO DATA
To the best of our knowledge, there is no publicly available dataset
that can be used to evaluate the performance of ultrasonic echo-based
depth estimation. We therefore build a data collection system and
collect a real echo dataset, which we call TUS-Echo.
Data Collection System. The overview of our data collection
system is shown in Fig. 3a. Our system consists of sensors and
sound acquisition devices mounted on a stable cart with suspension.
Four omni-directional ultrasonic microphones (Earthworks M30)
are mounted in a tetrapod shape using clamp arms, and these and
an ultrasound-compatible high-resolution loudspeaker (EDIFIER
S1000MK2) are connected to a PC via an audio interface (TASCAM US-4x4HR). The reason for using four microphones is that
depth map estimation requires capturing the 3D direction of arrival
of the echoes, and to accomplish this, the time difference of arrival
in each of the three directions relative to the reference microphone
needs to be measured. A depth camera (Intel RealSense D400) is
placed in front of the cart for acquiring ground truth depth maps.
Data Collection. The recording environment is a near-rectangular
reverberant studio of 4 m (width) × 10 m (depth) × 3 m (height). We
emitted two types of up-chirp signals from the loudspeaker at each
recording location and direction in the studio; one was an ultrasonic
chirp from 20 kHz to 48 kHz, and the other was an audible chirp
from 1 Hz to 48 kHz. The two types of echoes corresponding to
the two sound sources and a raw depth map of 128 × 128 pixels
were recorded in temporal synchronization. The duration of each
echo sample was 1 second with 96 kHz sampling rate, which was
sufficiently long to accommodate the chirp echoes. We collected
the data at 1,000 distinct locations and orientations, resulting in the
number of samples is 1,000 originated from different room impulse
responses (RIRs). We split the data into training/validation and test
sets in the ratio of 9:1 (896 and 104, respectively). A few examples
of the depth maps in our dataset are visualized in Fig. 3b.
