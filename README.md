# HashMap
import java.util.HashMap;
import java.util.Map;  
import java.util.Set;
class Hashmap {
    public void main(){
        
        //create - {key=value}
        HashMap<Integer,Character> map=new HashMap<>();
        
        //insert-put
        map.put(1,'A');
        map.put(2,'B');
        map.put(3,'C');
        map.put(4,'D');
        map.put(5,'E');
        map.put(6,'C');
        map.put(7,'F');
        
        System.out.println(map);
        
        /* key is always unique. key's value can be updated(which is printed corresponding to its previous map) if key exists,
         *  otherwise new map is added 
         */ 
        map.put(1,'C');   //updated
        map.put(19,'F');  //added
        System.out.println(map);
        
        //search (for a key)
        if(map.containsKey(5))
        System.out.println("5 key is present in the map");
        else
        System.out.println("5 key is not present in the map");
        
        //to get a value 
        System.out.println(map.get(7));  //from an existing key 
        System.out.println(map.get(21));  //from a non-existing key-returns null
        
        //remove
        map.remove(5);
        System.out.println(map);
        
        //Iteration in HashMap(also, called for Map & Set package)
        
        // 1. entrySet
        for(Map.Entry<Integer,Character> e: map.entrySet())   //variable 'e' contains all the pairs of map
        System.out.println(e.getKey());
        
        // 2. keySet
    }
}
