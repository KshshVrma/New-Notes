import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    
	    ArrayList<Integer> arr=new ArrayList<>(Arrays.asList(1,6,7,8,5));
	    arr.add(2);
	    arr.add(3);
	    arr.add(2);
	int[] arr2={1,3,4,5};
	String[] str=("Hello_World").split("_");
	StringBuilder sot =new StringBuilder("hello world today is sunday");
	sot.append(" and monday");
System.out.println(sot.toString());
	for(int i=0;i<str.length;i++){
	    System.out.println(str[i]);
	}

	   // ArrayList<
	    Map<Integer, Integer>mp =new HashMap<>();
	    Set<Integer> st=new HashSet<>();
	    
	    	for(int i=0;i<arr2.length;i++){
	    	    st.add(arr2[i]);
	    	          mp.put(arr.get(i), mp.getOrDefault(arr2[i], 0)+1);
	    
	}
	    
	    for(int i=0;i<arr.size();i++){
	        mp.put(arr.get(i), mp.getOrDefault(arr.get(i), 0)+1);
	        st.add(arr.get(i));
	    }
	    
	    
	    for(Map.Entry<Integer,Integer> et: mp.entrySet()){
	        if(et.getValue()> 1){
	        System.out.print(et.getKey()+ " "+ ">");
	        System.out.println(et.getValue());}
	    }
	    Iterator<Integer> it=st.iterator();
	    System.out.println("next");
	   while(it.hasNext()){
	       int k=it.next();
	       if(k%2==1){
	       System.out.println(k);
	       it.remove();}
	   }
	   st.remove(2);

	    for(int i=0;i<st.size();i++){
	        System.out.println(st.contains(arr.get(i))+ " "+ arr.get(i));
	    }
	    
		System.out.println("Hello World");
	}
}