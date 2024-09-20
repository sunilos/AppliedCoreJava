```java
package com.sunilos.p04controlstmt;

/**
 * DO-WHILE लूप का उदाहरण वर्ग
 * 
 * यह प्रोग्राम DO-WHILE लूप के उपयोग को प्रदर्शित करता है, जो यह सुनिश्चित करता है कि लूप का शरीर
 * कम से कम एक बार चलाया जाए, भले ही प्रारंभ में शर्त गलत हो।
 * 
 * @version 1.0
 * @since 16 Nov 2014
 * @author Sunil Sahu
 * @Copyright (c) Sunil Sahu
 * @url www.sunilbooks.com
 */

public class DoWhileLoop {

    public static void main(String[] args) {

        // स्थानीय चर i को 0 से प्रारंभ करें
        int i = 0;

        // लूप तब तक चलाएं जब तक i 5 से कम है
        do {
            // i का वर्तमान मान और संदेश प्रिंट करें
            System.out.println(i + " Hello Do While");
            // i को 1 से बढ़ाएं
            i++;
        } while (i < 5); // लूप तब तक चलता है जब तक i 5 से कम है
    }
}
```

### व्याख्या:
- **`do` ब्लॉक**: इस ब्लॉक के अंदर का कोड कम से कम एक बार चलेगा, इसके बाद शर्त की जांच की जाएगी।
- **`while (i < 5)`**: यह शर्त प्रत्येक पुनरावृत्ति के बाद जांची जाती है। यदि सही है, तो लूप जारी रहता है; यदि गलत है, तो लूप समाप्त हो जाता है।
- **आउटपुट**: प्रोग्राम `i` के मान 0 से 4 तक प्रिंट करता है, प्रत्येक के बाद "Hello Do While" संदेश।