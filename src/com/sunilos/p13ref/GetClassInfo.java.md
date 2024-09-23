
```java
package com.sunilos.p13ref;

import java.lang.reflect.Constructor;
import java.lang.reflect.Field;
import java.lang.reflect.Method;
import java.util.Date;
import com.sunilos.p06oop.Person;

/**
 * Create instance of a class using reflection API and print the class
 * information.
 * 
 * @version 1.0
 * @since 16 Nov 2014
 * @author Sunil Sahu
 * @Copyright (c) Sunil Sahu
 * @url www.sunilbooks.com
 */
public class GetClassInfo {

    public static void main(String[] args) throws Exception {

        // Obtain the Class object for the Person class
        Class<?> c = Class.forName("com.sunilos.p06oop.Person");

        // Create an instance of the Person class
        Person person = (Person) c.newInstance();

        // Set person information
        person.setName("Abhay");
        person.setAddress("Sadar Bazar");
        person.setDateOfBirth(new Date());

        // Print class details
        System.out.println("Class Information");
        System.out.println("\tName: " + c.getName());
        System.out.println("\tPackage: " + c.getPackage());
        System.out.println();

        // Get field information
        Field[] fields = c.getFields();
        System.out.println("Field Information");

        // Iterate over all fields and print their names and types
        for (Field f : fields) {
            System.out.println("\tName: " + f.getName());
            System.out.println("\tType: " + f.getType());
        }
        System.out.println();

        // Get class constructors
        Constructor<?>[] ctrs = c.getConstructors();
        System.out.println("Constructor Information");

        // Iterate over all constructors and print their names and parameter types
        for (Constructor<?> ctr : ctrs) {
            System.out.println("\tName: " + ctr.getName());
            Class<?>[] params = ctr.getParameterTypes();
            if (params.length > 0) {
                System.out.println("\tConstructor Parameter Types");
                for (Class<?> p : params) {
                    System.out.println("\t\t" + p.getName());
                }
            }
            System.out.println();
        }

        // Get class methods
        Method[] methods = c.getMethods();
        System.out.println("Method Information");

        // Iterate over all methods and print their names, return types, and parameter types
        for (Method m : methods) {
            System.out.println("\tName: " + m.getName());
            System.out.println("\tReturn Type: " + m.getReturnType());
            Class<?>[] params = m.getParameterTypes();
            if (params.length > 0) {
                System.out.println("\tMethod Parameter Types");
                for (Class<?> p : params) {
                    System.out.println("\t\t" + p.getName());
                }
            }
            System.out.println();
        }
    }
}
```

### Explanation:
- **Reflection API**: This code uses Java's Reflection API to inspect and manipulate the `Person` class at runtime.
- **Class Object**: It obtains the `Class` object for the `Person` class using `Class.forName()`, which allows access to class metadata.
- **Creating an Instance**: An instance of `Person` is created using `newInstance()`, allowing the code to set properties on the object.
- **Class Information**: The class name and package are printed for identification.
- **Field Information**: It retrieves and prints all public fields of the `Person` class, including their names and types.
- **Constructor Information**: It retrieves all constructors of the class, printing their names and any parameters they accept.
- **Method Information**: Finally, it retrieves all methods, printing their names, return types, and any parameters they accept.

