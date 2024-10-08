```java
package com.sunilos.p07exception;

/**
 * एक ही try ब्लॉक के उपयोग का प्रदर्शन करता है जिसमें 
 * विभिन्न प्रकार की एक्सेप्शंस को संभालने के लिए 
 * कई catch ब्लॉक्स होते हैं।
 * 
 * @version 1.0
 * @since 16 Nov 2014
 * @author Sunil Sahu
 * @Copyright (c) Sunil Sahu
 * @url www.sunilbooks.com
 */
public class MultiCatchHandling {

    public static void main(String[] args) {

        String name = "Vijay"; // प्रदर्शन के लिए नमूना स्ट्रिंग

        try {
            // स्ट्रिंग की लंबाई प्राप्त करें
            System.out.println(name.length());
            // स्ट्रिंग का 7वां अक्षर प्राप्त करने का प्रयास करें
            System.out.println(name.charAt(6));
        } catch (NullPointerException e) {
            // यह ब्लॉक तब निष्पादित होता है जब 'name' null है
            System.out.println("नाम null नहीं हो सकता");
        } catch (StringIndexOutOfBoundsException e) {
            // यह ब्लॉक तब निष्पादित होता है जब स्ट्रिंग की लंबाई 7 अक्षरों से कम हो
            System.out.println("स्ट्रिंग छोटी है");
        }

    }
}
```

### व्याख्या:

- **उद्देश्य:** `MultiCatchHandling` क्लास एक ही `try` ब्लॉक का उपयोग करके कई संभावित एक्सेप्शंस को संभालने का तरीका प्रदर्शित करती है जो उसके भीतर के कोड से उत्पन्न हो सकती हैं।

- **Try ब्लॉक:** `try` ब्लॉक के भीतर का कोड `name` स्ट्रिंग पर दो ऑपरेशन करने का प्रयास करता है: इसकी लंबाई प्राप्त करना और इसके सातवें अक्षर को एक्सेस करना। यदि ये ऑपरेशन किसी भी समस्या का सामना करते हैं, तो वे एक्सेप्शंस को फेंक सकते हैं।

- **Catch ब्लॉक्स:**
  - **NullPointerException:** यह कैच ब्लॉक उन मामलों को संभालता है जहां `name` वेरिएबल `null` है, जिससे प्रॉपर्टीज़ या मेथड्स को एक्सेस करते समय `NullPointerException` नहीं उठती। यह एक संदेश आउटपुट करता है जो बताता है कि नाम null नहीं हो सकता।
  
  - **StringIndexOutOfBoundsException:** यह कैच ब्लॉक उन परिस्थितियों को संबोधित करता है जहां स्ट्रिंग में 7 अक्षरों से कम होते हैं, जिससे एक ऐसा इंडेक्स एक्सेस करने का प्रयास होता है जो मौजूद नहीं है। यह एक संदेश आउटपुट करता है जो बताता है कि स्ट्रिंग बहुत छोटी है।

- **त्रुटि हैंडलिंग:** कई कैच ब्लॉक्स का उपयोग करके, प्रोग्राम विभिन्न त्रुटि परिदृश्यों के लिए विशिष्ट फीडबैक प्रदान कर सकता है, जिससे उपयोगकर्ता को यह स्पष्ट होता है कि क्या गलत हुआ। यह दृष्टिकोण मजबूती और उपयोगकर्ता अनुभव को बेहतर बनाता है क्योंकि यह एक्सेप्शंस को सुचारू रूप से संभालता है।
