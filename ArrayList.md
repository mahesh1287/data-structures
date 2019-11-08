Array List in Java.

1.	ArrayList<E> extends AbstractList<E>
 implements List<E>, RandomAccess, Cloneable, java.io.Serializable
2.	Internally It uses Object[] to store the objects.
3.	Initial capacity of ArrayList is 10
4.	When the object array becomes full then a new object array of 50% more size is created and elements are copied to this new array.
5.	Elements are stored one after the another, elements can be accessed by index. When we need to add elements in between the elements are moved to adjacent place in right direction.
6.	How elements are searched inside arraylist?
list.contains(elementToSearch); method is called.
Internally linear search using for loop is executed to perform search.
It calls indexOf(elementToSearch) is called.
Index of method returns first occurrence of the element 
Inside the for loop it uses equals method to verify the elements to be searched.
If you need custom search to work efficiently then override the equals method based on the properties of the custom object.
Example
     public class ArrayListDemo {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		List<Employee> list = new ArrayList<>();
		Employee e1 = new Employee(1,"Mahesh","SDOS", 12.78);
		list.add(e1);
		Employee e2 = new Employee(2,"Dilip","Core", 22);
		
		list.add(e2);
		//contains calls indexOf function, which uses equals of Employee class
		System.out.println(list.contains(e1));

	}


7.	When to use ArrayList?
When you need faster random access, give index and it will return the element in the constant time.
8.	What about deletion or adding?
ArrayList since it uses object arrays elements are moved to right while adding and to left while deleting it may cost over head if it has million elements to it.
