### binpacker
---
https://github.com/zhuangsirui/binpacker

```go
buffer := new(bytes.Buffer)
packer := binpacker.NewPacker(binary.BigEndian, buffer)
packer.PushByte(0x01)
packer.PushBytes([]byte{0x02, 0x03})
packer.PushUint16(math.MxUint16)

buffer := new(bytes.Buffer)
packer := binpacker.NewPacker(binary.BigEndian, buffer)
packer.Pushbyte(0x01).PushBytes([]byte{0x02, 0x03}).PushUint16(math.MaxUint16)
packer.Error()

buffer := new(bytes.Buffer)
packer := binpacker.NewPacker(binary.BigEndian, buffer)
unpacker := binpacker.Newpacker.NewUnpacker(binary.BigEndian, buffer)
packer.PushByte(0x01)
packer.PushUint16(math.MaxUint16)

var val1 byte
var val2 uint16
var err error
val1, err = unpacker.ShiftByte()
val2, err = unpacker.ShiftUint16()

var val1 byte
var val2 uint16
var err error
unpacker.FetchByte(&val1).FetchUint16(&val2)
unpacker.Error()

```

```sh
go get github.com/zhuangsirui/binpacker
```

```
```


