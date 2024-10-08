```java
package com.sunilos.p08collection;

import java.util.ArrayList;
import java.util.Collection;

/**
 * संग्रह निर्माण, तत्व जोड़ने और सभी तत्वों पर पुनरावृत्ति का परीक्षण करता है।
 * 
 * @version 1.0
 * @since 16 Nov 2014
 * @author Sunil Sahu
 * @Copyright (c) Sunil Sahu
 * @url www.sunilbooks.com
 */
public class TestCollection {

    public static void main(String[] args) {

        // ArrayList प्रकार का एक संग्रह बनाना
        Collection c = new ArrayList(); // लचीलापन के लिए Collection संदर्भ का उपयोग करना

        // संग्रह में तत्व जोड़ें
        c.add("Bura mat Dekho"); // इंडेक्स #0 पर एक स्ट्रिंग तत्व जोड़ता है
        c.add("Bura mat Suno");  // इंडेक्स #1 पर एक स्ट्रिंग तत्व जोड़ता है
        c.add("Bura mat Kaho");  // इंडेक्स #2 पर एक स्ट्रिंग तत्व जोड़ता है

        // संग्रह में तत्वों की संख्या का आउटपुट
        System.out.println("संग्रह की लंबाई: " + c.size());

        // foreach कथन का उपयोग करके संग्रह के सभी तत्व प्रिंट करें
        System.out.println("\nसंग्रह के तत्व ");
        for (Object ele : c) {
            System.out.println(ele); // संग्रह में प्रत्येक तत्व प्रिंट करें
        }

        // संग्रह को एक ऐरे में परिवर्तित करें
        Object[] oArray = c.toArray(); // संग्रह को एक Object ऐरे में परिवर्तित करता है

        System.out.println("\nपरिवर्तित ऐरे के तत्व");

        // foreach कथन का उपयोग करके ऐरे के सभी तत्व प्रिंट करें
        for (Object ele : oArray) {
            String s = (String) ele; // Object को प्रिंट करने के लिए String में कास्ट करें
            System.out.println(s); // ऐरे से प्रत्येक स्ट्रिंग तत्व प्रिंट करें
        }
    }
}
```

### व्याख्या:

1. **आयात:** क्लास `ArrayList` और `Collection` को `java.util` पैकेज से आयात करती है ताकि संग्रहों के साथ काम किया जा सके।

2. **क्लास घोषणा:** `TestCollection` एक सार्वजनिक क्लास है जो Java में संग्रहों के साथ मूल कार्यों को प्रदर्शित करने के लिए डिज़ाइन की गई है।

3. **मुख्य विधि:**
   - **संग्रह प्रारंभ करना:** एक `ArrayList` बनाई जाती है और इसे एक `Collection` प्रकार के वेरिएबल (`c`) द्वारा संदर्भित किया जाता है, जो कार्यान्वयन में लचीलापन प्रदान करता है।
   - **तत्व जोड़ना:** संग्रह में तीन स्ट्रिंग तत्व जोड़े जाते हैं। जोड़ने का क्रम उनके संबंधित इंडेक्स के अनुसार है।
   - **आकार आउटपुट:** संग्रह का आकार प्राप्त किया जाता है और प्रिंट किया जाता है, जिससे यह पता चलता है कि इसमें कितने तत्व हैं।
   - **पुनरावृत्ति और प्रिंटिंग:** एक foreach लूप का उपयोग करके संग्रह पर पुनरावृत्ति की जाती है, प्रत्येक तत्व को प्रिंट किया जाता है।
   - **ऐरे रूपांतरण:** `toArray` विधि को संग्रह को एक ऐरे (`oArray`) में परिवर्तित करने के लिए कॉल किया जाता है।
   - **ऐरे प्रिंटिंग:** एक और foreach लूप नए बनाए गए ऐरे पर पुनरावृत्ति करता है, प्रत्येक तत्व को प्रिंट करने से पहले `String` में कास्ट करता है।

यह क्लास प्रभावी रूप से दिखाती है कि संग्रह कैसे बनाया जाए, तत्व कैसे जोड़े जाएं, और उन पर पुनरावृत्ति की जाए, साथ ही संग्रह को एक ऐरे में कैसे परिवर्तित किया जाए।
