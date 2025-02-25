# collection-framework-linked-list-and-array-list
package collection.framework.linked.list.and.array.list;
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
import java.util.Scanner;
/**
 *
 * @author 1BSCCSA44
 */
public class CollectionFrameworkLinkedListAndArrayList {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
      LinkedList<Integer> linkedList = new LinkedList();
ArrayList<Integer> arrayList = new ArrayList();
List<Integer> commonList;  
Scanner scanner = new Scanner(System.in);
System.out.print("Enter integers separated by spaces:");
String input = scanner.nextLine();
String[] elements = input.split("\\s+");
for (String element : elements) {
int number = Integer.parseInt(element);
linkedList.add(number);
arrayList.add(number);
System.out.println("Initial Linked List: "+ linkedList);
System.out.println("Initial Array List: " + arrayList);
System.out.print("Enter elements to be added (separated by spaces):");
String elementsToAddInput = scanner.nextLine();
String[] elementsToAdd = elementsToAddInput.split("\\s+");
linkedList.addFirst(Integer.parseInt(elementsToAdd[0]));
}
arrayList.add(0,Integer.parseInt(elementsToAdd[0]));
linkedList.addLast(Integer.parseInt(elementsToAdd[1]));
arrayList.add(Integer.parseInt(elementsToAdd[1]));
        System.out.println("Final Linked List:"+ linkedList);
        System.out.println("Final Array List:" + arrayList);
        scanner.close();

        // TODO code application logic here
    }
    
}
output
Enter integers separated by spaces:1 2 3 4 5 6 7
Initial Linked List: [1]
Initial Array List: [1]
Enter elements to be added (separated by spaces):1
Initial Linked List: [1, 1, 2]
Initial Array List: [1, 2]
Enter elements to be added (separated by spaces):78
Initial Linked List: [78, 1, 1, 2, 3]
Initial Array List: [1, 2, 3]
Enter elements to be added (separated by spaces):96587
Initial Linked List: [96587, 78, 1, 1, 2, 3, 4]
Initial Array List: [1, 2, 3, 4]

