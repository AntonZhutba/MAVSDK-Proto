# MAVSDK-Proto
Collection of proto files used by gRPC in MAVSDK

## Description

MAVSDK is made of a backend in C++ called mavsdk_server, exposing a protobuf API that can be used by different frontends, such as [MAVSDK-Python](https://dev.dedrone.com/dt/striker/MAVSDK-Python), [MAVSDK-Java](https://dev.dedrone.com/dt/striker/MAVSDK-Java).

The mavsdk_server is made of different components responsible for different parts of the API. Each component defines a protobuf interface in the form of a directory containing `*.proto` files in this repository.

The proto files defining the components are located into [protos](protos), and the protobuf plugins generating the bindings in the different languages are located into [pb_plugins](pb_plugins).


## Usage

Please read: [Additional information](https://mavsdk.mavlink.io/main/en/cpp/contributing/plugins.html#create-a-plugin)
 
Edit or add .proto

In the protos/ directory:
• Find the desired .proto file (e.g. action.proto) and edit it
or
• Add a new .proto file for your plugin (e.g. my_plugin.proto)

Update submodule in [MAVSDK]((https://dev.dedrone.com/dt/striker/mavsdk/)) project

```sh
git submodule update --init --recursive
```
Install protoc_gen_mavsdk

```sh
cd proto

pip install -r requirements.txt

pip install  .

```

Use the guide to generate code from [MAVSDK]((https://dev.dedrone.com/dt/striker/mavsdk/))


## Authors and acknowledgment
Show your appreciation to those who have contributed to the project.

## License
Open source projects, origin repo [MAVSDK-Proto](https://github.com/mavlink/MAVSDK-Proto)

## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
