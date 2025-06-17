![GitHub release](https://img.shields.io/github/v/release/eclipse-cyclonedds/cyclonedds?include_prereleases)
[![Build Status](https://dev.azure.com/eclipse-cyclonedds/cyclonedds/_apis/build/status/Pull%20requests?branchName=master)](https://dev.azure.com/eclipse-cyclonedds/cyclonedds/_build/latest?definitionId=4&branchName=master)
[![Coverity Status](https://scan.coverity.com/projects/19078/badge.svg)](https://scan.coverity.com/projects/eclipse-cyclonedds-cyclonedds)
[![Coverage](https://img.shields.io/azure-devops/coverage/eclipse-cyclonedds/cyclonedds/4/master)](https://dev.azure.com/eclipse-cyclonedds/cyclonedds/_build/latest?definitionId=4&branchName=master)
[![License](https://img.shields.io/badge/License-EPL%202.0-blue)](https://choosealicense.com/licenses/epl-2.0/)
[![License](https://img.shields.io/badge/License-EDL%201.0-blue)](https://choosealicense.com/licenses/edl-1.0/)
[![Website](https://img.shields.io/badge/web-cyclonedds.io-blue)](https://cyclonedds.io)
[![Community](https://img.shields.io/badge/discord-join%20community-5865f2)](https://discord.gg/BkRYQPpZVV)



# This branch supports CycloneDDS over FreeRTOS-Plus-TCP stack on FreeRTOS.  
CycloneDDS looks have support on FreeRTOS+LWIP Stack,  
however lacking FreeRTOS-Plus-TCP Stack support  
This change managed to add +TCP support  

 * base CycloneDDS version 0.10.2
 * begin: FreeRTOS_Plus_TCP IP stack */
 cmakedefine DDSRT_WITH_FREERTOSTCP 1
 cmakedefine DDSRT_TRANS_UDP 1
 cmakedefine DDSRT_TRANS_TCP 1
 cmakedefine DDSRT_TRANS_RAWETH 1
 cmakedefine DDSRT_TRANS_NONE 1
 * end: FreeRTOS_Plus_TCP IP stack */

    [Changes]
      +TCP socket
      ddsrt header and source
      sockaddr ifaddr
      .init_array section
      log sink
      multicast/unicast peer define in xml
      TLS-Thread_Local_Storage FreeRTOS SW impl instead of toolchain
      sock_waitset
      sock fdset
      sendmsg/recvmsg for UDP
      dds_align from 0.10.2
      FragmentSize for jumbo and normal

    [Issue]
     CycloneDDS perf to OPT






# Eclipse Cyclone DDS
Eclipse Cyclone DDS is a very performant and robust open-source implementation of the [OMG DDS specification](https://www.omg.org/spec/DDS/1.4/About-DDS/).
Cyclone DDS is developed completely in the open as an Eclipse IoT project (see [eclipse-cyclone-dds](https://projects.eclipse.org/projects/iot.cyclonedds)) with a growing list of [adopters](https://iot.eclipse.org/adopters/?#iot.cyclonedds) (if you're one of them, please add your [logo](https://github.com/EclipseFdn/iot.eclipse.org/issues/new?template=adopter_request.md)).
It is a tier-1 middleware for the Robot Operating System [ROS 2](https://docs.ros.org/en/rolling/).

Link:
https://github.com/polejoe/cycloneDDS/blob/master/README.md
