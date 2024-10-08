
```java
package com.sunilos.p12swing;

/**
 * Enum क्लास `Day` में हफ्ते के दिनों का प्रतिनिधित्व करने वाले स्थायी मान शामिल हैं।
 * 
 * प्रत्येक स्थायी मान एक दिन के लिए है, और एनम एक ऐसा मेथड प्रदान करता है जो 
 * संबंधित सप्ताह का दिन अनुक्रमांक (रविवार के लिए 0 से शुरू) प्राप्त करता है।
 * 
 * @संस्करण 1.0
 * @तारीख 16 नवम्बर 2014
 * @लेखक सुनिल साहू
 * @कॉपीराइट (c) सुनिल साहू
 * @वेबसाइट www.sunilbooks.com
 */
public enum Day {

    // हफ्ते के दिनों का प्रतिनिधित्व करने वाले स्थायी मान
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY;

    /**
     * हफ्ते में दिन का अनुक्रमांक लौटाता है, जहां रविवार 0 है और शनिवार 6 है।
     * 
     * @return दिन का अनुक्रमांक, जो रविवार के लिए 0 से शुरू होता है।
     */
    public int getWeekDay() {

        // स्विच स्टेटमेंट का उपयोग करके प्रत्येक एनम स्थायी मान को उसके अनुक्रमांक से जोड़ें
        switch (this) {
            case SUNDAY:
                return 0; // रविवार
            case MONDAY:
                return 1; // सोमवार
            case TUESDAY:
                return 2; // मंगलवार
            case WEDNESDAY:
                return 3; // बुधवार
            case THURSDAY:
                return 4; // गुरुवार
            case FRIDAY:
                return 5; // शुक्रवार
            case SATURDAY:
                return 6; // शनिवार
            default:
                return -1; // डिफ़ॉल्ट केस, अगर कोई अप्रत्याशित स्थिति हो
        }
    }
}
```

### व्याख्या:
1. **एनम स्थायी मान**:
   - एनम `Day` में हफ्ते के दिनों (`SUNDAY` से `SATURDAY` तक) के लिए स्थायी मान शामिल हैं।

2. **`getWeekDay()` मेथड**:
   - यह मेथड एक पूर्णांक लौटाता है जो दिन के अनुक्रमांक का प्रतिनिधित्व करता है, जिसमें `0` रविवार के लिए और `6` शनिवार के लिए है।

3. **स्विच स्टेटमेंट**:
   - स्विच स्टेटमेंट वर्तमान एनम स्थायी मान (`this`) की जांच करता है और प्रत्येक दिन के लिए संबंधित पूर्णांक मान लौटाता है।

4. **डिफ़ॉल्ट केस**:
   - एक डिफ़ॉल्ट केस प्रदान किया गया है, हालांकि सामान्य परिस्थितियों में यह नहीं पहुंचेगा क्योंकि सभी एनम स्थायी मानों को स्पष्ट रूप से संभाला गया है। यह फॉलबैक के रूप में `-1` लौटाता है।
