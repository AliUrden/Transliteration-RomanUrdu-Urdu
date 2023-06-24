# Transliteration-RomanUrdu-Urdu
This repository contains an implementation of transliteration from Roman Urdu to Urdu (roman2urdu) and Urdu to Roman Urdu (urdu2roman). The goal of this assignment is to perform basic text manipulation techniques for the Urdu language. The system of Romanisation used most often by native speakers differs from formal systems presented in English language sources. The implemented functions aim to address the shortcomings of existing Roman Urdu schemes and provide a reversible transliteration that allows proper pronunciation of Urdu words.

# Contents
* Introduction
* Background
* Implementation Challenges
* Solution
  * urdu2roman
  * roman2urdu
* Usage
  
# Introduction
Roman Urdu is the name used for the Urdu language written with the Latin script, also known as the Roman script. The Urdu language is written in a different style compared to English, making typing a challenging task. Roman Urdu has gained popularity due to its ease of use. In this assignment, the goal is to implement transliteration techniques for converting text between Roman Urdu and Urdu script.

# Background
Transliteration involves converting text from one script to another while preserving the pronunciation. The implementation of transliteration techniques requires identifying grapheme boundaries within words and determining character-level patterns. This assignment focuses on developing a technique for transliterating between Roman Urdu and Urdu scripts.

# Implementation Challenges
The implementation of transliteration techniques poses several challenges. The following decisions need to be made:

1. How can character-level patterns be detected in text?
2. How simple and elegant is the solution?
3. How can the approach be evaluated?

# Solution
The provided code implements two functions: urdu2roman and roman2urdu. These functions perform transliteration between Roman Urdu and Urdu scripts.

# urdu2roman
The urdu2roman function transliterates Urdu words to Roman Urdu. It uses a dictionary (urdu_to_roman_dict) to map Urdu characters to their Roman Urdu equivalents. The function iterates through each character in the input word and constructs the corresponding Roman Urdu word by considering the character's position within the word. It handles digits and English alphabets as they are and replaces Urdu characters with their Roman Urdu counterparts.

# roman2urdu
The roman2urdu function performs the reverse transliteration, converting Roman Urdu words to Urdu script. It uses a dictionary (roman_to_urdu_dict) to map Roman Urdu characters to their Urdu equivalents. The function applies various rules to handle specific cases, such as replacing specific sequences of characters or modifying vowel sequences. It iteratively applies the rules and replaces the characters to obtain the corresponding Urdu word.

# Usage
To use the transliteration functions, follow these steps:

1. Import the required libraries, such as nltk.
2. Define the Urdu sentence or Roman Urdu word to be transliterated.
3. Call the urdu2roman or roman2urdu function with the input sentence/word as the argument.
4. The function will return the transliterated output.
5. Display or further process the output as desired.

# Example usage:
```
import nltk

# Define Urdu sentence
urdu_sentence = "معافی سے بڑھ کے اب رہا کیا ہے؟"

# Transliterate Urdu sentence to Roman Urdu
roman_urdu_sentence = urdu2roman(urdu_sentence)
print(roman_urdu_sentence)

# Define Roman Urdu word
roman_urdu_word = "Maafi"

# Transliterate Roman Urdu word to Urdu script
urdu_word = roman2urdu(roman_urdu_word)
print(urdu_word)
```

# Note:
Before using the urdu2roman and roman2urdu functions, you need to ensure that the necessary libraries (such as nltk) are imported and the dictionary mappings (urdu_to_roman_dict and roman_to_urdu_dict) are properly defined in your code.
Make sure to adapt the code to your specific programming environment and ensure that the required dependencies are installed.
