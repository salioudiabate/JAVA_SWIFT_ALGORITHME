


## Compare 2 strings 

 

       public static boolean compare(String x, String y){
           
            if(x.length()!=y.length())
                return false;
     
            for (int i = 0; i <x.length() ; i++) {
                if(x.charAt(i)!=y.charAt(i))
                    return false;
            }
            
            return true;
        }

    

## Frequence d'apparition

    public class FrequenceApparition {
    
        public static void main(String[] args) {
              String s = "sdfsd sdfsdf sdfsdf sdfs f ";
            String s1 = "sdfsd";
            int fre = 0;
           String[] array=s.split(" ");
            //algorithme
            for (int i = 0; i < array.length; i++) {
                if (s1.equals(array[i])) {
                    fre++;
                }
            }
            
            System.err.println("frequence :  " + fre);
    
        }
    }

## inverser une chaine


            String chaine = "hello world";
            char[] inputStringArray = chaine.toCharArray();
            String reverseString = "";
    
            for (int i = inputStringArray.length - 1; i >= 0; i--) {
                reverseString += inputStringArray[i];
            }
    
            System.err.println("" + reverseString);

## inverser une phrase


 

     String chaine = "I love Java Programming"; 
            String[] temp = chaine.split(" ");
            String result = ""; 
      
    
            for (int i = 0; i < temp.length; i++) {
                
                if (i == temp.length - 1) 
                    result = temp[i] + result; 
                else
                    result = " " + temp[i] + result; 
            } 
            
            System.out.println(result);
    
## consonne voyelle


            char[] input = "hello world"
            char[] voyelle = "aeiouy".toCharArray();
            char[] consonne ="abcdfghjklmnpqrstvxz".toCharArray();
            int cons = 0;
            int voy = 0;
            
    
            //algorithme
            for (int i = 0; i < input.length; i++) {
                for (int j = 0; j < voyelle.length; j++) {
                    if (input[i] == voyelle[j]) {
                        voy++;
                    }
                }
    
                for (int j = 0; j < consonne.length; j++) {
                    if (input[i] == consonne[j]) {
                        cons++;
                    }
                }
    
            }
            
            System.err.println("consonne " + cons);
            System.err.println("voyelle " + voy);
    

## palindrome


    public static boolean isPalindrome(String s) {
        
                int i = 0;
                int j = s.length() - 1;
        
                while (i < j) {
                    if (s.charAt(i) != s.charAt(j)) {
                        return false;
                    }
        
                    i++;
                    j--;
                }
                return true;
            }

## UpperCase LowerCase



algo

    char maj[] = {'A', 'B', 'Z'};
    char min[] = {'a', 'b', 'z'};
    String input = "abz";
    char[] char_array = input.toCharArray();

    
    for (int k = 0; k < char_array.length; k++) {
        for (int l = 0; l < min.length; l++) {
            if (min[l] == char_array[k]) {
                char_array[k] = maj[l];
            }
        }
    }

    //affichage
    String res = new String(char_array);

## swap two string variables without using third or temp variable

    public static void main(String[] args) {
        String str1 = "Good", str2 = "morning";
    
        System.out.println("Strings before swapping: " + str1 + " " + str2);
    
        //Concatenate both the string str1 and str2 and store it in str1
        str1 = str1 + str2;
        //Extract str2 from updated str1
        str2 = str1.substring(0, (str1.length() - str2.length()));
        //Extract str1 from updated str1
        str1 = str1.substring(str2.length());
    
        System.out.println("Strings after swapping: " + str1 + " " + str2);
    }

  
  ## separate the individual characters from a string

      public static void main(String[] args) {
            String string = "characters";
    
            //Displays individual characters from given string
            System.out.println("Individual characters from given string:");
    
            //Iterate through the string and display individual character
            for (int i = 0; i < string.length(); i++) {
                System.out.print(string.charAt(i) + " ");
            }
        }

## find the largest & smallest word in a string

      public static void main(String[] args) {
        String string = "Hardships often prepare ordinary people for an extraordinary destiny";
        String word = "", small = "", large = "";
        String[] words = new String[100];
        int length = 0;

        //Add extra space after string to get the last word in the given string
        string = string + " ";

        for (int i = 0; i < string.length(); i++) {
            //Split the string into words
            if (string.charAt(i) != ' ') {
                word = word + string.charAt(i);
            } else {
                //Add word to array words
                words[length] = word;
                //Increment length
                length++;
                //Make word an empty string
                word = "";
            }
        }

        //Initialize small and large with first word in the string
        small = large = words[0];

        //Determine smallest and largest word in the string
        for (int k = 0; k < length; k++) {

            //If length of small is greater than any word present in the string
            //Store value of word into small
            if (small.length() > words[k].length()) {
                small = words[k];
            }

            //If length of large is less than any word present in the string
            //Store value of word into large
            if (large.length() < words[k].length()) {
                large = words[k];
            }
        }

        System.out.println("Smallest word: " + small);
        System.out.println("Largest word: " + large);
    }
## find the frequency of characters

     public static void main(String[] args) {
        String str = "picture perfect";
        int[] freq = new int[str.length()];
        int i, j;
    
        //Converts given string into character array
        char string[] = str.toCharArray();
    
        for (i = 0; i < str.length(); i++) {
            freq[i] = 1;
            for (j = i + 1; j < str.length(); j++) {
                if (string[i] == string[j]) {
                    freq[i]++;
    
                    //Set string[j] to 0 to avoid printing visited character
                    string[j] = '0';
                }
            }
        }
    
        //Displays the each character and their corresponding frequency
        System.out.println("Characters and their corresponding frequencies");
        for (i = 0; i < freq.length; i++) {
            if (string[i] != ' ' && string[i] != '0') {
                System.out.println(string[i] + "-" + freq[i]);
            }
        }
    }

## find the duplicate words in a string

    public static void main(String[] args) {
        String string = "Big black bug bit a big black dog on his big black nose";
        int count;
    
        //Converts the string into lowercase
        string = string.toLowerCase();
    
        //Split the string into words using built-in function
        String words[] = string.split(" ");
    
        System.out.println("Duplicate words in a given string : ");
        for (int i = 0; i < words.length; i++) {
            count = 1;
            for (int j = i + 1; j < words.length; j++) {
                if (words[i].equals(words[j])) {
                    count++;
                    //Set words[j] to 0 to avoid printing visited word
                    words[j] = "0";
                }
            }
    
            //Displays the duplicate word if count is greater than 1
            if (count > 1 && words[i] != "0") {
                System.out.println(words[i]);
            }
        }
    }

## find reverse of a string

     public static void main(String[] args) {
            String string = "Dream big";
            //Stores the reverse of given string
            String reversedStr = "";
    
            //Iterate through the string from last and add each character to variable reversedStr
            for (int i = string.length() - 1; i >= 0; i--) {
                reversedStr = reversedStr + string.charAt(i);
            }
    
            System.out.println("Original string: " + string);
            //Displays the reverse of given string
            System.out.println("Reverse of given string: " + reversedStr);
        }

##  one string is a rotation of another

    public static void main(String[] args) {
        String str1 = "abcde", str2 = "deabc";
    
        if (str1.length() != str2.length()) {
            System.out.println("Second string is not a rotation of first string");
        } else {
            //Concatenate str1 with str1 and store it in str1
            str1 = str1.concat(str1);
    
            //Check whether str2 is present in str1
            if (str1.indexOf(str2) != -1) {
                System.out.println("Second string is a rotation of first string");
            } else {
                System.out.println("Second string is not a rotation of first string");
            }
        }
    }

## find the longest repeating sequence in a string
**Input:**

str = "acbdfghybdf"

**Output:**

Longest repeating sequence: bdf

    1.  //Checks for the largest common prefix
    2.  public  static String lcp(String s, String t){
    3.  int n = Math.min(s.length(),t.length());
    4.  for(int i = 0; i < n; i++){
    5.  if(s.charAt(i) != t.charAt(i)){
    6.  return s.substring(0,i);
    7.  }
    8.  }
    9.  return s.substring(0,n);
    10.  }
    
    12.  public  static  void main(String[] args) {
    13.  String str = "acbdfghybdf";
    14.  String lrs="";
    15.  int n = str.length();
    16.  for(int i = 0; i < n; i++){
    17.  for(int j = i+1; j < n; j++){
    18.  //Checks for the largest common factors in every substring
    19.  String x = lcp(str.substring(i,n),str.substring(j,n));
    20.  //If the current prefix is greater than previous one
    21.  //then it takes the current one as longest repeating sequence
    22.  if(x.length() > lrs.length()) lrs=x;
    23.  }
    24.  }
    25.  System.out.println("Longest repeating sequence: "+lrs);
    26.  }

## find all possible subsets of a string

**Input:**

    str = "ABC"

**Output:**

    All subsets for given string are:
    A
    AB
    ABC
    B
    BC
    C

**program**
     public static void main(String[] args) {
    
            String str = "ABC";
            int len = str.length();
            
            //Total possible subsets for string of size n is n*(n+1)/2
            List arr=new ArrayList();
    
            //This loop maintains the starting character
            for (int i = 0; i < len; i++) {
                //This loop adds the next character every iteration for the subset to form and add it to the array
                for (int j = i; j < len; j++) {
                    arr.add(str.substring(i, j + 1));
                 
                }
            }
    
            //This loop prints all the subsets formed from the string.
            System.out.println("All subsets for given string are: ");
            for (int i = 0; i < arr.size(); i++) {
                System.out.println(arr.get(i));
            }
        }

## remove all the white spaces from a string

**Input:**

str1 = "Remove white spaces"

**Output:**

       public static void main(String[] args) {
    
            String str1 = "Remove white spaces";
    
            //Removes the white spaces using regex
            str1 = str1.replaceAll("\\s+", "");
    
            System.out.println("String after removing all the white spaces : " + str1);
        }

## find all the permutations of a string
**Input:**

    char str[] = "ABC" 

**Output:**

    All the permutations of the string are:
    ABC
    ACB
    BAC
    BCA
    CBA
    CAB

**Program**

    //Function for swapping the characters at position I with character at position j
    public static String swapString(String a, int i, int j) {
        char[] b = a.toCharArray();
        char ch;
        ch = b[i];
        b[i] = b[j];
        b[j] = ch;
        System.out.println(String.valueOf(b));
        return String.valueOf(b);
    }
    
    public static void main(String[] args) {
        String str = "ABC";
        int len = str.length();
        System.out.println("All the permutations of the string are: ");
        generatePermutation(str, 0, len);
    }
    
    //Function for generating different permutations of the string
    public static void generatePermutation(String str, int start, int end) {
        //Prints the permutations
        if (start == end - 1) {
            System.out.println(str);
        } else {
            for (int i = start; i < end; i++) {
                //Swapping the string by fixing a character
                str = swapString(str, start, i);
                //Recursively calling function generatePermutation() for rest of the characters
                generatePermutation(str, start + 1, end);
                //Backtracking and swapping the characters again.
                str = swapString(str, start, i);
            }
        }
    }

## to divide a string in 'N' equal parts.
**Input:**

    str = "aaaabbbbcccc"

**Output:**

    Equal parts of given string are
    aaaa
    bbbb
    cccc

**program**
     public static void main(String[] args) {
            String str = "aaaabbbbcccc";
    
            //Stores the length of the string
            int len = str.length();
            //n determines the variable that divide the string in 'n' equal parts
            int n = 3;
            int temp = 0, chars = len / n;
            //Stores the array of string
            String[] equalStr = new String[n];
            //Check whether a string can be divided into n equal parts
            if (len % n != 0) {
                System.out.println("Sorry this string cannot be divided into " + n + " equal parts.");
            } else {
                for (int i = 0; i < len; i = i + chars) {
                    //Dividing string in n equal part using substring()
                    String part = str.substring(i, i + chars);
                    equalStr[temp] = part;
                    temp++;
                }
                System.out.println(n + " equal parts of given string are ");
                for (int i = 0; i < equalStr.length; i++) {
                    System.out.println(equalStr[i]);
                }
            }
        }

## determine whether two strings are the anagram
**Input:**

    Two Strings are called the anagram if they contain the same characters. However, the order or sequence of the characters can be different.
    
    str1 = "Grab";
    str2 = "Brag";

**Output:**

    Both the strings are anagram.

**Program**

       public static void main(String[] args) {
            String str1 = "Brag";
            String str2 = "Grab";
    
            //Converting both the string to lower case.
            str1 = str1.toLowerCase();
            str2 = str2.toLowerCase();
    
            //Checking for the length of strings
            if (str1.length() != str2.length()) {
                System.out.println("Both the strings are not anagram");
            } else {
                //Converting both the arrays to character array
                char[] string1 = str1.toCharArray();
                char[] string2 = str2.toCharArray();
    
                //Sorting the arrays using in-built function sort ()
                Arrays.sort(string1);
                Arrays.sort(string2);
    
                //Comparing both the arrays using in-built function equals ()
                if (Arrays.equals(string1, string2) == true) {
                    System.out.println("Both the strings are anagram");
                } else {
                    System.out.println("Both the strings are not anagram");
                }
            }
        }

## Headingcount the total number of punctuation characters exists in a string

**Input:**

char str [] = "Good Morning! Mr. James Potter. Had your breakfast?"

**Output:**

If any character in the string is matched with ('!', "," ,"\'" ,";" ,"\"", ".", "-" ,"?"), increment the count by 1.

**Total number of punctuation characters exists in string: 4**

 

    public static void main(String[] args) {
            //Stores the count of punctuation marks
            int countPuncMarks = 0;
            String str = "Good Morning! Mr. James Potter. Had your breakfast?";
            for (int i = 0; i < str.length(); i++) {
                //Checks whether given character is punctuation mark
                if (str.charAt(i) == '!' || str.charAt(i) == ',' || str.charAt(i) == ';' || str.charAt(i) == '.' || str.charAt(i) == '?' || str.charAt(i) == '-'
                        || str.charAt(i) == '\'' || str.charAt(i) == '\"' || str.charAt(i) == ':') {
                    countPuncMarks++;
                }
            }
            System.out.println("Total number of punctuation characters exists in string: " + countPuncMarks);
        }
