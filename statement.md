```java runnable
// { autofold
import static java.nio.charset.StandardCharsets.UTF_8;
import java.util.Base64;
import java.util.Base64.Decoder;
import java.util.Base64.Encoder;

public class Main {

public static void main(String[] args) throws Exception {

// }

String string = "some random data";

// Encoding
Encoder encoder = Base64.getEncoder();
byte[] data = string.getBytes(UTF_8);
String encodedString = encoder.encodeToString(data);

System.out.println("Encoded: " + encodedString);

// Decoding
Decoder decoder = Base64.getDecoder();
byte[] bytes = decoder.decode(encodedString);
String decodedString = new String(bytes, UTF_8);

System.out.println("Decoded: " + decodedString);

//{ autofold

}

}
//}
```
