public class Linked_list {
    private class Node {
        int data;
        Node next;
        public void setData(int data) {
            this.data = data;
            this.next=null;
        }
    }
    private Node head;
    private int size;

    public Linked_list(){
        this.head=null;
        this.size=0;
    }
    public boolean isempty(){
        return head==null;
    }
    public void insertLast(int data){
        Node newNode = new Node();
        if(isempty()){
            head=newNode;
        }else{
            Node current=head;
            while (current.next!=null) {
                current=current.next;
            }
            current.next=newNode;
        }
        size++;
    }
    public int Listsize(){
        return size;
    }
    public void indrtAtpossition(int data,int position){
        if (position<0 || position > size) {
            throw new IndexOutOfBoundsException("Invalid position");
        }
        Node newNode=new Node();
        if(position==0){
            newNode.next=head;
            head=newNode;
        }else{
            Node current =head;
            for(int i=0;i<position-1;i++){
                current=current.next;
            }
            newNode.next=current.next;
            current.next=newNode;
        }
        size++;
    }
    public void deleteATPosition(int position){
        if(position==0){
            head=head.next;
        }else{
            Node current =head;
            for(int i=0;i<position-1;i++){
                current=current.next;
            }
            current.next=current.next.next;
        }
        size--;
    }
    public void traverseList(){
        if(isempty()){
            System.out.println("List is empty");
        }else{
            Node current=head;
            while (current!=null) {
                System.out.print(current.data+" ");
                current=current.next;
            }
            System.out.println();
        }
    }
    public static void main(String[] args) {
        LinkedList List =new LinkedList();
        List.insertLast(100);
        List.insertLast(200);
        List.insertLast(300);
        List.insertLast(400);
        List.insertLast(500);
        List.traverseList();
        System.out.println("List size: "+List.listSize());
        List.insertAtPosition(25, 4);
        List.traverseList();
        List.deleteAtPosition(2);
        List.traverseList();
        System.out.println("List size: "+List.listSize());
    }
}
