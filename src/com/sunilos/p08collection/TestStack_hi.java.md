```java
package com.sunilos.p08collection;

import java.util.Stack;

/**
 * Stack वर्ग का परीक्षण करें
 * 
 * @version 1.0
 * @since 16 Nov 2014
 * @author Sunil Sahu
 * @Copyright (c) Sunil Sahu
 * @url www.sunilbooks.com
 */

public class TestStack {

    public static void main(String[] args) {

        // तत्वों को रखने के लिए एक Stack उदाहरण बनाएं
        Stack stack = new Stack();

        // Stack में तत्वों को डालें
        stack.push("1"); // Stack के शीर्ष पर "1" जोड़ता है
        stack.push("2"); // Stack के शीर्ष पर "2" जोड़ता है
        stack.push("3"); // Stack के शीर्ष पर "3" जोड़ता है

        // Stack से शीर्ष वस्तु पर नज़र डालें बिना उसे हटाए
        Object objTop = stack.peek(); // "3" लौटाना चाहिए
        System.out.println(objTop); // शीर्ष वस्तु को प्रिंट करें

        // Stack से शीर्ष वस्तु को हटाएं, जो इसे भी हटा देता है
        Object obj3 = stack.pop(); // "3" को हटा देता है और लौटाता है
        System.out.println(obj3); // हटाई गई वस्तु को प्रिंट करें

        // Stack से अगली वस्तु को हटाएं
        Object obj2 = stack.pop(); // "2" को हटा देता है और लौटाता है
        System.out.println(obj2); // हटाई गई वस्तु को प्रिंट करें

        // Stack से अंतिम वस्तु को हटाएं
        Object obj1 = stack.pop(); // "1" को हटा देता है और लौटाता है
        System.out.println(obj1); // हटाई गई वस्तु को प्रिंट करें
    }
}
```

### व्याख्या:

1. **Imports:** `java.util` पैकेज से `Stack` वर्ग आयात किया गया है, जिससे हम स्टैक डेटा संरचना का उपयोग कर सकें।

2. **Class Declaration:** `TestStack` कक्षा `Stack` वर्ग का उपयोग करने का प्रदर्शन करती है।

3. **Main Method:**
   - **Stack Initialization:** `stack` नामक एक `Stack` उदाहरण बनाया गया है, जो तत्वों को रखने के लिए है।
   - **Pushing Elements:** 
     - तीन स्ट्रिंग ("1", "2", और "3") `push()` विधि का उपयोग करके स्टैक में डाली गई हैं। `push()` विधि का प्रत्येक कॉल स्टैक के शीर्ष पर एक तत्व जोड़ता है।
   - **Peeking at the Top Element:**
     - `peek()` विधि स्टैक के शीर्ष तत्व को प्राप्त करती है बिना उसे हटाए। इस मामले में, यह "3" लौटाती है।
     - शीर्ष तत्व को कंसोल में प्रिंट किया जाता है।
   - **Popping Elements:**
     - `pop()` विधि को तीन बार बुलाया गया है, जो हर बार शीर्ष तत्व को हटाती और लौटाती है।
     - `pop()` को कॉल करने पर हटाई गई वस्तु को प्रिंट किया जाता है: पहले "3", फिर "2", और अंत में "1"।

### मुख्य बिंदु:
- **LIFO संरचना:** स्टैक एक Last In, First Out (LIFO) सिद्धांत का पालन करता है, जिसका मतलब है कि अंतिम जोड़ा गया तत्व सबसे पहले हटाया जाता है।
- **विधियों का उपयोग:** 
  - `push()`: स्टैक के शीर्ष पर एक तत्व जोड़ता है।
  - `peek()`: शीर्ष तत्व को लौटाता है बिना उसे हटाए।
  - `pop()`: शीर्ष तत्व को हटाता और लौटाता है। 

यह कक्षा `Stack` वर्ग की मूल कार्यक्षमता को प्रभावी ढंग से दर्शाती है, यह प्रदर्शित करते हुए कि स्टैक से तत्वों को कैसे जोड़ा, पुनः प्राप्त और हटाया जाए।
