binary-spec
===========

```
/*
 * *PacketStruct
 *  |DATASIZE|RPC|DATA|CHECKSUM|
 *  DATASIZE=2byte
 *   CHECKSUM+RPC+DATAのサイズを格納
 *  RPC=2byte
 *   RPCの値を格納
 *  DATA=Xbyte
 *   RPCのデータを格納
 *   サイズはSIZE-6で算出可能
 *   送信可能サイズは65535byteまで
 *  CHECKSUM=4byte
 *   CRC32によるDATAのチェックサム値
 * *DATA Format
 *  int8    : 1byte
 *  int16   : 2byte
 *  int32   : 4byte
 *  int64   : 8byte
 *  uint8   : 1byte
 *  uint16  : 2byte
 *  uint32  : 4byte
 *  uint64  : 8byte
 *  float   : 4byte
 *  double  : 8byte
 *  string  : LENにSTRINGの長さを入れる
 *      |LEN|STRING|
 *      LEN=2byte
 *  enum    : int32として扱う
 *  array   : COUNTに個数を入れる
 *      |COUNT|DATA1|DATA2|DATA3|
 *      COUNT=2byte
 */
```
