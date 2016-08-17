# NetworkManagementModule
Calculating First Shortest Path and Second Shortest Path when a traffic in a perticular link increases it 
automatically switches to second shortest path from the source and removes the previously installed path.

This project uses POX controller.
Has two module PathCalculation and NetworkMonitoring.

PathCalculation is used to calculate shortest path whenever a connection is established between source and destination 
eg: ping src dst, installing/removing the flows in the switches which are involved in the calculated path.

NetworkMonitoring Module is used to collect Network statistics at regular intervals like delay,bandwidth,throughput.
when ever the delay increases precribed limit delay module calls PathCalculation Module for installing new flows and removing 
previous.

The extensioin of calculating second shortest path and switching it over when delay increases is extension added
to the original code from OpenNetmon project.
Thanks to OpenNetmon Team.
