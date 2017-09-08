# Collaborative Robotic System Experimental Data
This repository contains raw measurement data from the Cybersecurity for Smart Manufacturing Testbed's Collaborative Robotic System. The testbed is located at the National Institute of Standards and Technology (NIST) in Gaithersburg, Maryland.

## Background
NIST has constructed a testbed to measure the performance impact induced by cybersecurity technologies on Industrial Control Systems (ICS). The testbed allows researchers to emulate real-world industrial manufacturing processes and their control systems without the need to replicate an entire factory environment or its machinery.

__Figure 1.__ View of the workcell with the two robotic arms, four simulated machining stations, and queue.
![_robots]

The focus of this repository is the Robotic Enclave of the testbed, which is comprised of two robotic arms that emulate a material handling application, known as “machine tending.” Robotic machine tending uses robots to interact with the machinery, performing operations a human operator would normally perform (e.g., the loading and unloading of parts, opening and closing of machine doors, activating operator control panel buttons). In the enclave, parts are transported collaboratively through simulated sequential machining operations, known as “stations.” The enclave was designed and constructed to be reconfigurable, allowing numerous types of operational methodologies, network topologies, and industrial networking protocols to be investigated \[[NISTIR 8177][_IR8177]\].

__Figure 2.__ Network diagram of the collaborative robotics system.
![_netdiag]

## Measurements
Measurement data are in the raw format obtained directly from the testbed systems. All files from an experiment are stored together in a single folder, whose name denotes the experiment date and tool description. An example folder structure is described below.

```
  .
  +-- Experiments - Low Security Level
  |   +-- 2017-08-15 - Baseline
  |   |   +-- ExperimentMetadata.dat
  |   |   +-- PLCPartData.csv
  |   |   +-- PLCPerformanceData.csv
  |   |   +-- ServerPerfLog_vController1.csv
  |   |   +-- ServerPerfLog_vController2.csv
  |   |   +-- RobotPerfLog_R1.log
  |   |   +-- RobotPerfLog_R2.log
  +-- Experiments - Moderate Security Level
  +-- Experiments - High Security Level
```
Details about each measurement data file and measurements can be found in the [METADATA][_meta] file.

A detailed description of the collaborative robotics system can be found in the documents [NISTIR 8177, "Metrics and Key Performance Indicators for Robotic Cybersecurity Performance Analysis"][_IR8177], and [NISTIR 8089, "ICS Cybersecurity Performance Testbed Design Report"][_IR8089].

## Cybersecurity for Smart Manufacturing Systems Project
> Manufacturers are hesitant to adopt common security technologies, such as encryption and device authentication, due to concern for potential negative performance impacts in their systems. This is exacerbated by a threat environment that has changed dramatically with the appearance of advanced persistent attacks specifically targeting industrial systems, such as Stuxnet in 2010, Shamoon in 2012 and BlackEnergy in 2015. Smart manufacturing systems need to be protected from vulnerabilities that may arise as a result of their increased connectivity, use of wireless networks and sensors, and use of widespread information technology. The Cybersecurity for Smart Manufacturing Systems project will deliver a cybersecurity risk management framework with supporting guidelines, methods, metrics and tools to enable manufacturers, technology providers, and solution providers to assess and assure cybersecurity for smart manufacturing systems while addressing the demanding performance, reliability, and safety requirements of these systems. The cybersecurity risk management framework with supporting guidelines, methods, metrics and tools will stimulate manufacturer adoption and enable effective use of security technologies, leading to smart manufacturing systems that offer security, reliability, resiliency and continuity in the face of disruption and major incidents.

More information about the project can be found at [the project landing page][_CSMS].

## License
Data from the robotic system is licensed to the public domain. For more information, please see the [LICENSE][_license] file.

## Disclaimer
Certain commercial entities, equipment, or materials may be identified in this
document in order to describe an experimental procedure or concept adequately.
Such identification is not intended to imply recommendation or endorsement by
the [National Institute of Standards and Technology (NIST)][_NIST], nor is it
intended to imply that the entities, materials, or equipment are necessarily
the best available for the purpose.

[_NIST]: http://www.nist.gov
[_IR8089]: http://nvlpubs.nist.gov/nistpubs/ir/2015/NIST.IR.8089.pdf
[_IR8177]: http://nvlpubs.nist.gov/nistpubs/ir/2017/NIST.IR.8177.pdf
[_CSMS]: https://www.nist.gov/programs-projects/cybersecurity-smart-manufacturing-systems
[_netdiag]: ./readme_assets/RobotEnclave_NetworkDiagram.png "Collaborative Robotic System Network Diagram"
[_meta]: ./METADATA.md
[_robots]: ./readme_assets/roboticsystem.jpg "Collaborative robotic system workcell"
[_license]: ./LICENSE.md
