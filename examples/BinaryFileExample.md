```java



import java.io.*;
 
import static org.math.io.files.BinaryFile.*;
import static org.math.io.parser.ArrayString.*;
 
public class BinaryFileExample {
        public static void main(String[] args) {
 
                // NOTE THAT ONLY 1D ARRAYS ARE SUPPORTED IN BINARY FORMAT
                
                double[] a = { 1.0, 2.0, 3.0, 4.0 };
 
                // write file in binary
                writeDoubleArray(new File("a.dat"), a, "LITTLE_ENDIAN");
 
                // read these file
                double[] a_read = readDoubleArray(new File("a.dat"), "LITTLE_ENDIAN");
 
                // print in Command Line the results using the org.math.io.parser.ArrayString static methods
                System.out.println("a = \n" + printDoubleArray(a));
                System.out.println("a_read = \n" + printDoubleArray(a_read));
        }
}


```
