# openshift-f5-env-setup
Setup connectivity between the OpenShift ramp node and F5 BIGIP router 


Setup F5 BIGIP Host:
--------------------
To setup the F5 BIGIP host connectivity to the OpenShift cluster, you need the IP address of the node that
you have designated to be the OpenShift Cluster's ramp node and then just run:

    $ sudo ./setup-f5-sdn  <ramp-node-ip-address>    
    $ #  E.g.sudo ./setup-f5-sdn  10.3.89.191
    

Setup OpenShift Ramp Node:
--------------------------
To setup the ramp node as a bridge connecting the OpenShift cluster and the F5 BIGIP host, you need the IP address
of the F5 node's internal interface and the type of OpenShift SDN plugin configured for your OpenShift cluster.

    $ sudo ./setup-ramp-node-sdn  <f5-host-internal-ip>  <openshift-sdn-plugin>
    $ # E.g. sudo ./setup-ramp-node-sdn  10.3.89.235 "multitenant"
