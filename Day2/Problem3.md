# Problem 3
## Bridge network
##### This is the default network that is created when you install Docker. It allows containers to communicate with each other and with the host system.

## Host network
##### This network allows containers to use the host's network stack and IP addresses. This can be useful if you want to access a container directly from the host system, or if you need to bypass the built-in Docker networking.

## Overlay network
##### This network type allows containers to communicate with each other across multiple Docker hosts. This is useful for distributed applications that span multiple hosts.

## Macvlan network
##### This network type allows you to assign a MAC address to a container, giving it a unique identity on the network. This can be useful if you want to connect a container directly to a physical network, or if you need to use network-level protocols that are not supported by the default Docker networking.

## Custom networks
##### Docker also allows you to create custom networks, using drivers such as "bridge," "overlay," or "macvlan." This can be useful if you want to customize the network configuration for a specific use case.
