"# protobuf-java" 

****** How it works ******

1. Write a .proto description of the data structure you wish to store
2. From that the protocol buffer compiler creates a class that implements automatic encoding and parsing of the protocol buffer data with an efficient binary format.
3. The generated class provides getters and setters for the fields that make up a protocol buffer and takes care of the details of reading and writing the protocol buffer  as a unit.
4. Importantly, the protocol buffer format supports the idea of extending the format over time in such a way that the code can still read data encoded with the old format.

****** Compiling Protocol Buffers ******

1. You need to download the latest proto compiler from https://github.com/protocolbuffers/protobuf/releases

2. then run the following:- protoc -I=$SRC_DIR --java_out=$DST_DIR $SRC_DIR/addressbook.proto

    e.g. .\protoc-3.9.0-win64\bin\protoc.exe -I=.\ --java_out=.\ .\addressbook.proto

3. The java out spits out an AddressBookProtos.java java.class file in the com.examples.tutorial package