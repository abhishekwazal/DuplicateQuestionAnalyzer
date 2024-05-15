# DuplicateQuestionAnalyzer

## Description 

<img src="https://user-images.githubusercontent.com/20265851/132982880-34ee5dc5-c358-4105-ae02-2eca800acb47.png" height="222px"/>

Quora is a place to gain and share knowledge—about anything. It’s a platform to ask questions and connect with people who contribute unique insights and quality answers. This empowers people to learn from each other and to better understand the world.

Over 100 million people visit Quora every month, so it's no surprise that many people ask similarly worded questions. Multiple questions with the same intent can cause seekers to spend more time finding the best answer to their question, and make writers feel they need to answer multiple versions of the same question. Quora values canonical questions because they provide a better experience to active seekers and writers, and offer more value to both of these groups in the long term.

## Problem statement 

“Given two question are they duplicates of each other”

## Data set 

source : https://www.kaggle.com/c/quora-question-pairs/overview/description

COLUMNS 

    - id : tuple unique id
    - qid1/qid2 : question id of question1/question2 
    - question1/question2 : actual question in string 
    - is_duplicate : is question1 is duplicate of question2? (1:YES/0:NO) 
    
<img width="656" alt="Screenshot1" src="https://github.com/abhishekwazal/DuplicateQuestionAnalyzer/assets/95206285/ff122d9b-3ee3-4008-8249-18e8579212cb">

## Basic Feature Addition 
 - ____q1len____ = Length of q1
 - ____q2len____ = Length of q2
 - ____q1_num_words____ = Number of words in Question 1
 - ____q2_num_words____ = Number of words in Question 2
 - ____word_Common____ = (Number of common unique words in Question 1 and Question 2)
 - ____word_Total____ =(Total num of words in Question 1 + Total num of words in Question 2)
 - ____word_share____ = (word_common)/(word_Total)
   
![Screenshot 2024-05-15 175754](https://github.com/abhishekwazal/DuplicateQuestionAnalyzer/assets/95206285/d9170762-4289-4a47-8339-7c3dc07d5dc3)

## Advanced Feature Addition 
- __cwc_min__ :  Ratio of common_word_count to min lenghth of word count of Q1 and Q2 
- __cwc_max__ :  Ratio of common_word_count to max lenghth of word count of Q1 and Q2 
- __last_word_eq__ :  Check if First word of both questions is equal or not
- __first_word_eq__ :  Check if First word of both questions is equal or not
- __abs_len_diff__ :  Abs. length difference
- __mean_len__ :  Average Token Length of both Questions
- __longest_substr_ratio__ :  Ratio of length longest common substring to min lenghth of token count of Q1 and Q2

![Screenshot 2024-05-15 181441](https://github.com/abhishekwazal/DuplicateQuestionAnalyzer/assets/95206285/dd542c11-3192-4d36-b80d-bc8c1ce1c293)
