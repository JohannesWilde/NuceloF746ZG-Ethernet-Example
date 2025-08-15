# STM32 NUCLEO-F746ZG Example

My attempts at getting the NUCLEO-F746ZG to work with RTOS and Ethernet - as it was more than a simple plug-and-play and I could not find any ready-made examples exactly for this board.

The main points of interest were:

  - https://community.st.com/t5/stm32-mcus-embedded-software/stack-overflow-in-freeartos-and-ethernet/td-p/782263
  - https://community.st.com/t5/stm32-mcus-boards-and-hardware/how-to-skip-the-interruption-while-debugging-stm32f746-discovery/td-p/320355

  - For CMake configuration do not use the STM32 Cube IDE. Use the latter only for coding. And for code configuration always use Cube MX.
  - For opening the project created via Cube MX in Cube IDE go to File -> New -> Project -> ST -> STM32 CMake Project and select "Project with existing CMake sources".
  - For faster builds
  	- select Ninja as generator [Project Properties -> C/C++ Build -> CMake Settings -> Generator] and
  	- add "-j N", with N being the number of parallel jobs, to the CMake arguments [Project Properties -> C/C++ Build -> Behaviour -> Build Arguments]
  