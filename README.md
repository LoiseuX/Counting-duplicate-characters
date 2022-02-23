# Counting-duplicate-characters

    import java.util.HashMap;
    import java.util.Map;
    import java.util.Map.Entry;
    import java.util.Scanner;
    public class CountingDuplicateCharacters {
    public static void main(String[] args) {
       
        //get input from the user
        //Scanner in = new Scanner(System.in);
        //System.out.print("Input String: ");
        //String input = in.nextLine();
        //System.out.println(input);
        
        //given input
        System.out.println("Duplicate Characters in a given string: ");
        String input = "Hellllloo ooo ooo";
        
        //create hashmap
       Map<Character, Integer> countDuplicateMap = new HashMap<> ();
       
       //Converts this string to a new character array
       char[] charToArray = input.toCharArray();
       
       for(char c : charToArray){
       
           if(countDuplicateMap.containsKey(c)){
               
               //get value by key and increment it's value by a
               countDuplicateMap.put(c, countDuplicateMap.get(c) + 1);
           }
           else{
               countDuplicateMap.put(c,1);
           } 
       }
       
       for(Entry<Character, Integer> entry : countDuplicateMap.entrySet()){
           if(entry.getValue() > 1){
               System.out.println(entry.getKey() + " : " + entry.getValue());
             
                       
           } 
       }
    
    }
}
