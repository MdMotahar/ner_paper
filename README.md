```bash
Task Description: You are working as a named
entity recognition expert and your task is to label a
given text with named entity labels. Your task is to
identify and label any named entities present in the
text. The named entity labels that you will be using
are NUM (number), EVENT (event), MISC (miscellanous ner tags),
PER (person),T&T (terms and titles of different
entities.), LOC (location), GPE (geographical and
political entities), UNIT (measurements
of money, number, rate, age, etc.),
D&T (Data & Time), ORG (Organization).

Note: Please use BIO annotation schema to complete this task.
Please make sure to label each word
of the entity with the appropriate prefix (“B” for
the first word of the entity, “I” for any non-initial
word of the entity). For words which are not part
of any named entity, you should return “O”. Do not provide any
explanations for the output.

Demonstrations: Optional. 
[Input:['একেকটি', 'বই', '৭০', 'থেকে', '৯০', 'টাকা',
'বা', 'এর', 'চেয়েও', 'বেশি', 'দামের', '।'] ,
Output:['O', 'O', 'B-NUM', 'O', 'B-NUM', 'B-UNIT', 'O', 'O',
'O', 'O', 'O', 'O']],
[Input:['কলেজে', 'ভর্তিতে', 'কোন', 'আসন',
'সংকট', 'হবে', 'না', 'বলে', 'জানিয়েছে', 'শিক্ষাবোর্ড', '।'] ,
Output:['B-ORG', 'O', 'O', 'O', 'O', 'O', 'O','O',
'O', 'B-ORG', 'O']],
[Input:['আমরা', 'আমাদের', 'জাতীয়', 'স্বার্থ',
'রক্ষার', 'জন্য', 'লড়াই', 'করছি', ',',
'আমাদের', 'নাগরিকদের', 'ও', 'জনগণের', 'স্বার্থের', 'সুরক্ষায়', 'লড়ছি', '।'] ,
Output:['O', 'O', 'O', 'O', 'O', 'O', 'O', 'O', 'O',
'O', 'B-PER', 'O', 'B-PER', 'O', 'O', 'O', 'O']],
[Input:['মেঘলা', ',', 'নীলাচল', ',', 'প্রান্তিক',
'লেক', 'শৈলপ্রপাত', ',', 'চিম্বুক', 'পাহাড়', ',',
'নীলগিরিসহ', 'দর্শনীয়স্থানে', 'ভিড়', 'করছেন', 'তারা', '।'] ,
Output:['B-LOC', 'O', 'B-LOC', 'O', 'B-LOC',
'I-LOC', 'I-LOC', 'O', 'B-LOC', 'I-LOC', 'O',
'B-LOC', 'O', 'O', 'O', 'O', 'O']],
[Input:['এদিকে', ',', 'নতুন', 'বছর', 'উপলক্ষ্যে',
'দেওয়া', 'ভাষণে', ',', 'ইউক্রেন', 'সংকটের', 'জন্য',
'আবারো', 'পশ্চিমাদের','দায়ী', 'করেন', 'রুশ', 'প্রেসিডেন্ট', '।'] ,
Output:['O', 'O', 'O', 'O', 'O', 'O', 'O', 'O',
'B-GPE', 'O', 'O', 'O', 'B-PER', 'O', 'O', 'B-GPE', 'B-PER', 'O']],
[Input:['আজও', 'কুয়াশার', 'চাদরে', 'ঢাকা', 'রাজধানী', '।'] ,
Output:['B-D&T', 'O', 'O', 'O', 'O', 'O']],
[Input:['আটকে', 'যায়', 'রাজশাহীর', 'ফজলি',
'আমের', 'জিআই', 'সনদ', '।'] ,
Output:['O', 'O', 'B-GPE', 'B-MISC', 'I-MISC', 'B-MISC', 'I-MISC', 'O']],
[Input:['ইংরেজী', 'নতুন', 'বছর', 'বরণের', 'অন্যতম',
'আকর্ষণ', 'যুক্তরাষ্ট্রের', 'নিউইয়র্কের',
'টাইসস্কয়ারের', 'নিউ', 'ইয়ার', 'ইভের', 'আয়োজন', '।'] ,
 Output:['O', 'O', 'O', 'O', 'O',
 'O', 'B-GPE', 'B-GPE', 'B-LOC', 'B-EVENT', 'I-EVENT',
'I-EVENT', 'O', 'O']],
[Input:['গিনিজ', 'ওয়ার্ল্ড', 'রেকর্ডসে', 'নাম', 'লিখিয়েছে', 'সংযুক্ত',
'আরব', 'আমিরাতের', 'বর্ষবরণের', 'আয়োজন', '।'] ,
Output:['B-T&T', 'I-T&T', 'I-T&T', 'O', 'O', 'B-GPE',
'I-GPE', 'I-GPE', 'O', 'O', 'O']],
[Input:['তবু', 'বেশ', 'লাগছে', 'বসে', 'থাকতে', '।'] ,
Output:['O', 'O', 'O', 'O', 'O', 'O']],

Input: ['স্বাধীন', 'বাংলাদেশে', 'মাথাপিছু', 'আয়', 'ছিলো', '৮৮', 'ডলার', '।']
Output:
```
