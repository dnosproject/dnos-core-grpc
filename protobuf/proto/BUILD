load("@io_grpc_grpc_java//:java_grpc_library.bzl", "java_grpc_library")

PROTO_SOURCE_ROOT = "protobuf/proto"

DEPS = [
    ":ClusterId_proto",
    ":ConnectPoint_proto",
    ":Criterion_proto",
    ":DeviceDescription_proto",
    ":DeviceEnums_proto",
    ":DeviceEvent_proto",
    ":DeviceId_proto",
    ":Device_proto",
    ":DisjointPath_proto",
    ":EventNotification_proto",
    ":FlowEntryEnums_proto",
    ":FlowEntry_proto",
    ":FlowRuleEnums_proto",
    ":FlowRule_proto",
    ":HostDescription_proto",
    ":HostEnums_proto",
    ":HostEvent_proto",
    ":HostId_proto",
    ":HostLocation_proto",
    ":Host_proto",
    ":InboundPacket_proto",
    ":Instruction_proto",
    ":Instructions_proto",
    ":LinkDescription_proto",
    ":LinkEnums_proto",
    ":LinkEvent_proto",
    ":Link_proto",
    ":MastershipRole_proto",
    ":OutboundPacket_proto",
    ":PacketContext_proto",
    ":PacketEnums_proto",
    ":PacketEvent_proto",
    ":Path_proto",
    ":PortDescription_proto",
    ":PortEnums_proto",
    ":PortStatistics_proto",
    ":Port_proto",
    ":ProviderId_proto",
    ":RegionEnums_proto",
    ":Region_proto",
    ":Services_proto",
    ":ControlMessages_proto",
    ":Status_proto",
    ":TopologyCluster_proto",
    ":TopologyEdge_proto",
    ":TopologyGraph_proto",
    ":TopologyVertex_proto",
    ":Topology_proto",
    ":TrafficTreatment_proto",
    ":TraficSelector_proto",
    ":OpenFlowPacketCtx_proto",
    ":Dpid_proto",
    "@com_google_protobuf//:any_proto",
]

#### Java
java_grpc_library(
    name = "onos-core-protobuf-services-proto",
    srcs = [":Services_proto"],
    visibility = ["//visibility:public"],
    deps = [
        ":onos-protobuf-models-proto",
    ],
)

java_proto_library(
    name = "onos-protobuf-models-proto",
    visibility = ["//visibility:public"],
    deps = DEPS,
)

#### grpc-integration app ####
proto_library(
    name = "ControlMessages_proto",
    srcs = ["grpcintegration/ControlMessagesProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    deps = [
             ":ClusterId_proto",
             ":Device_proto",
             ":Host_proto",
             ":Path_proto",
             ":Port_proto",
             ":TopologyCluster_proto",
             ":Topology_proto",
             ":FlowRule_proto",
         ],
)


proto_library(
    name = "Status_proto",
    srcs = ["grpcintegration/StatusProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "EventNotification_proto",
    srcs = ["grpcintegration/EventNotificationProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":LinkEvent_proto",
        ":PacketContext_proto",
        ":OpenFlowPacketCtx_proto"
    ],
)

proto_library(
    name = "Services_proto",
    srcs = ["grpcintegration/ServicesProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
             ":ConnectPoint_proto",
             ":ControlMessages_proto",
             ":DeviceId_proto",
             ":Device_proto",
             ":EventNotification_proto",
             ":FlowRule_proto",
             ":HostId_proto",
             ":Host_proto",
             ":OutboundPacket_proto",
             ":Port_proto",
             ":Status_proto",
             ":TopologyGraph_proto",
             ":Topology_proto",
         ],
)

### net ###

### device ###
proto_library(
    name = "DeviceDescription_proto",
    srcs = ["net/device/DeviceDescriptionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":DeviceEnums_proto"],
)

proto_library(
    name = "DeviceEnums_proto",
    srcs = ["net/device/DeviceEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "DeviceEvent_proto",
    srcs = ["net/device/DeviceEventProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":DeviceEnums_proto",
        ":Device_proto",
        ":Port_proto",
    ],
)

proto_library(
    name = "PortDescription_proto",
    srcs = ["net/device/PortDescriptionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":PortEnums_proto"],
)

proto_library(
    name = "PortEnums_proto",
    srcs = ["net/device/PortEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "PortStatistics_proto",
    srcs = ["net/device/PortStatisticsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

### flow ###
## criteria ##
proto_library(
    name = "Criterion_proto",
    srcs = ["net/flow/criteria/CriterionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

## instrcutions ##
proto_library(
    name = "Instruction_proto",
    srcs = ["net/flow/instructions/InstructionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":Port_proto"],
)

proto_library(
    name = "Instructions_proto",
    srcs = ["net/flow/instructions/InstructionsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "FlowEntryEnums_proto",
    srcs = ["net/flow/FlowEntryEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "FlowEntry_proto",
    srcs = ["net/flow/FlowEntryProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":FlowEntryEnums_proto"],
)

proto_library(
    name = "FlowRuleEnums_proto",
    srcs = ["net/flow/FlowRuleEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "FlowRule_proto",
    srcs = ["net/flow/FlowRuleProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":FlowRuleEnums_proto",
        ":TrafficTreatment_proto",
        ":TraficSelector_proto",
    ],
)

proto_library(
    name = "TraficSelector_proto",
    srcs = ["net/flow/TrafficSelectorProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":Criterion_proto"],
)

proto_library(
    name = "TrafficTreatment_proto",
    srcs = ["net/flow/TrafficTreatmentProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":Instruction_proto",
        ":Instructions_proto",
    ],
)

#### host ####

proto_library(
    name = "HostDescription_proto",
    srcs = ["net/host/HostDescriptionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":HostLocation_proto"],
)

proto_library(
    name = "HostEnums_proto",
    srcs = ["net/host/HostEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "HostEvent_proto",
    srcs = ["net/host/HostEventProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":HostEnums_proto",
        ":Host_proto",
    ],
)

#### link ####

proto_library(
    name = "LinkDescription_proto",
    srcs = ["net/link/LinkDescriptionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":ConnectPoint_proto",
        ":LinkEnums_proto",
    ],
)

proto_library(
    name = "LinkEnums_proto",
    srcs = ["net/link/LinkEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "LinkEvent_proto",
    srcs = ["net/link/LinkEventProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":LinkEnums_proto",
        ":Link_proto",
    ],
)

### packet ####

proto_library(
    name = "InboundPacket_proto",
    srcs = ["net/packet/InboundPacketProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":ConnectPoint_proto"],
)

proto_library(
    name = "PacketContext_proto",
    srcs = ["net/packet/PacketContextProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":InboundPacket_proto",
        ":OutboundPacket_proto",
    ],
)

proto_library(
    name = "OutboundPacket_proto",
    srcs = ["net/packet/OutboundPacketProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":TrafficTreatment_proto"],
)

proto_library(
    name = "PacketEnums_proto",
    srcs = ["net/packet/PacketEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "PacketEvent_proto",
    srcs = ["net/packet/PacketEventProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":OutboundPacket_proto",
        ":PacketEnums_proto",
    ],
)

#### region ####

proto_library(
    name = "RegionEnums_proto",
    srcs = ["net/region/RegionEnumsProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "ConnectPoint_proto",
    srcs = ["net/ConnectPointProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "Device_proto",
    srcs = ["net/DeviceProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":DeviceEnums_proto"],
)

proto_library(
    name = "DisjointPath_proto",
    srcs = ["net/DisjointPathProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":Path_proto"],
)

proto_library(
    name = "HostId_proto",
    srcs = ["net/HostIdProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "HostLocation_proto",
    srcs = ["net/HostLocationProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":ConnectPoint_proto"],
)

proto_library(
    name = "Host_proto",
    srcs = ["net/HostProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":HostId_proto",
        ":HostLocation_proto",
        ":ProviderId_proto",
    ],
)

proto_library(
    name = "Link_proto",
    srcs = ["net/LinkProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":ConnectPoint_proto",
        ":LinkEnums_proto",
        ":ProviderId_proto",
    ],
)

proto_library(
    name = "MastershipRole_proto",
    srcs = ["net/MastershipRoleProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "Path_proto",
    srcs = ["net/PathProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":Link_proto"],
)

proto_library(
    name = "Port_proto",
    srcs = ["net/PortProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":PortEnums_proto"],
)

proto_library(
    name = "ProviderId_proto",
    srcs = ["net/ProviderIdProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "Region_proto",
    srcs = ["net/RegionProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":RegionEnums_proto"],
)

proto_library(
    name = "DeviceId_proto",
    srcs = ["net/DeviceIdProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

### topology ####
proto_library(
    name = "Topology_proto",
    srcs = ["net/topology/TopologyProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "TopologyEdge_proto",
    srcs = ["net/topology/TopologyEdgeProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":Link_proto"],
)

proto_library(
    name = "TopologyGraph_proto",
    srcs = ["net/topology/TopologyGraphProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    deps = [
        ":TopologyEdge_proto",
        ":TopologyVertex_proto",
    ],
)

proto_library(
    name = "TopologyVertex_proto",
    srcs = ["net/topology/TopologyVertexProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [":DeviceId_proto"],
)

proto_library(
    name = "ClusterId_proto",
    srcs = ["net/topology/ClusterIdProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "TopologyCluster_proto",
    srcs = ["net/topology/TopologyClusterProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
    deps = [
        ":ClusterId_proto",
        ":TopologyVertex_proto",
    ],
)


## protocols

proto_library(
    name = "Dpid_proto",
    srcs = ["protocols/openflow/DpidProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    visibility = ["//visibility:public"],
)

proto_library(
    name = "OpenFlowPacketCtx_proto",
    srcs = ["protocols/openflow/OpenFlowPacketContextProto.proto"],
    proto_source_root = PROTO_SOURCE_ROOT,
    deps = [":Dpid_proto"],
    visibility = ["//visibility:public"],
)