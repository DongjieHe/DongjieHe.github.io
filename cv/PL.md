1. <java.util.IdentityHashMap$KeySet: java.util.Iterator iterator()>
```
public java.util.Iterator iterator() {
    java.util.IdentityHashMap$KeyIterator $stack1;
    java.util.IdentityHashMap$KeySet l0;
    java.util.IdentityHashMap $stack2;

    l0 := @this: java.util.IdentityHashMap$KeySet;
    $stack1 = new java.util.IdentityHashMap$KeyIterator;
    $stack2 = l0.<java.util.IdentityHashMap$KeySet: java.util.IdentityHashMap this$0>;
    specialinvoke $stack1.<java.util.IdentityHashMap$KeyIterator: void <init>(java.util.IdentityHashMap,java.util.IdentityHashMap$1)>($stack2, null);
    return $stack1;
}
void <init>(java.util.IdentityHashMap, java.util.IdentityHashMap$1) {
    java.util.IdentityHashMap$KeyIterator l0;
    java.util.IdentityHashMap l1;
    java.util.IdentityHashMap$1 l2;

    l0 := @this: java.util.IdentityHashMap$KeyIterator;
    l1 := @parameter0: java.util.IdentityHashMap;
    l2 := @parameter1: java.util.IdentityHashMap$1;
    specialinvoke l0.<java.util.IdentityHashMap$KeyIterator: void <init>(java.util.IdentityHashMap)>(l1);
    return;
}
private void <init>(java.util.IdentityHashMap) {
    java.util.IdentityHashMap$KeyIterator l0;
    java.util.IdentityHashMap l1;

    l0 := @this: java.util.IdentityHashMap$KeyIterator;
    l1 := @parameter0: java.util.IdentityHashMap;
    l0.<java.util.IdentityHashMap$KeyIterator: java.util.IdentityHashMap this$0> = l1;
    specialinvoke l0.<java.util.IdentityHashMap$IdentityHashMapIterator: void <init>(java.util.IdentityHashMap,java.util.IdentityHashMap$1)>(l1, null);
    return;
}
```
2. <java.util.LinkedList: java.util.LinkedList$Entry addBefore(java.lang.Object,java.util.LinkedList$Entry)>
```
private java.util.LinkedList$Entry addBefore(java.lang.Object, java.util.LinkedList$Entry) {
    java.util.LinkedList$Entry $stack4, l2, $stack5, l3, $stack6, $stack7;
    java.lang.Object l1;
    java.util.LinkedList l0;
    int $stack8, $stack9, $stack10, $stack11;

    l0 := @this: java.util.LinkedList;
    l1 := @parameter0: java.lang.Object;
    l2 := @parameter1: java.util.LinkedList$Entry;
    $stack4 = new java.util.LinkedList$Entry;
    $stack5 = l2.<java.util.LinkedList$Entry: java.util.LinkedList$Entry previous>;
    specialinvoke $stack4.<java.util.LinkedList$Entry: void <init>(java.lang.Object,java.util.LinkedList$Entry,java.util.LinkedList$Entry)>(l1, l2, $stack5);
    l3 = $stack4;
    $stack6 = l3.<java.util.LinkedList$Entry: java.util.LinkedList$Entry previous>;
    $stack6.<java.util.LinkedList$Entry: java.util.LinkedList$Entry next> = l3;
    $stack7 = l3.<java.util.LinkedList$Entry: java.util.LinkedList$Entry next>;
    $stack7.<java.util.LinkedList$Entry: java.util.LinkedList$Entry previous> = l3;
    $stack8 = l0.<java.util.LinkedList: int size>;
    $stack9 = $stack8 + 1;
    l0.<java.util.LinkedList: int size> = $stack9;
    $stack10 = l0.<java.util.LinkedList: int modCount>;
    $stack11 = $stack10 + 1;
    l0.<java.util.LinkedList: int modCount> = $stack11;
    return l3;
}
void <init>(java.lang.Object, java.util.LinkedList$Entry, java.util.LinkedList$Entry) {
    java.util.LinkedList$Entry l0, l2, l3;
    java.lang.Object l1;

    l0 := @this: java.util.LinkedList$Entry;
    l1 := @parameter0: java.lang.Object;
    l2 := @parameter1: java.util.LinkedList$Entry;
    l3 := @parameter2: java.util.LinkedList$Entry;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    l0.<java.util.LinkedList$Entry: java.lang.Object element> = l1;
    l0.<java.util.LinkedList$Entry: java.util.LinkedList$Entry next> = l2;
    l0.<java.util.LinkedList$Entry: java.util.LinkedList$Entry previous> = l3;
    return;
}
```
3. inner class
```
static class UnmodifiableEntrySet<K, V> extends Collections.UnmodifiableSet<Map.Entry<K, V>> {
      UnmodifiableEntrySet(Set<? extends Map.Entry<? extends K, ? extends V>> param2Set) {
        super(param2Set);
      }
      public Iterator<Map.Entry<K, V>> iterator() {
        return new Iterator<Map.Entry<K, V>>() {
            Iterator<? extends Map.Entry<? extends K, ? extends V>> i = Collections.UnmodifiableMap.UnmodifiableEntrySet.this.c.iterator();
            public boolean hasNext() {
              return this.i.hasNext();
            }
            public Map.Entry<K, V> next() {
              return new Collections.UnmodifiableMap.UnmodifiableEntrySet.UnmodifiableEntry<K, V>(this.i.next());
            }
          };
      }
}
```
4. <java.util.LinkedList: java.lang.Object[] toArray()>
```
public java.lang.Object[] toArray() {
    java.util.LinkedList l0;
    int $stack4, $stack7, l2;
    java.lang.Object[] l1;
    java.util.LinkedList$Entry $stack5, $stack6, l3;
    java.lang.Object $stack8;

    l0 := @this: java.util.LinkedList;
    $stack4 = l0.<java.util.LinkedList: int size>;
    l1 = newarray (java.lang.Object)[$stack4];
    l2 = 0;
    $stack5 = l0.<java.util.LinkedList: java.util.LinkedList$Entry header>;
    l3 = $stack5.<java.util.LinkedList$Entry: java.util.LinkedList$Entry next>;
 label1:
    $stack6 = l0.<java.util.LinkedList: java.util.LinkedList$Entry header>;
    if l3 == $stack6 goto label2;
    $stack7 = l2;
    l2 = l2 + 1;
    $stack8 = l3.<java.util.LinkedList$Entry: java.lang.Object element>;
    l1[$stack7] = $stack8;
    l3 = l3.<java.util.LinkedList$Entry: java.util.LinkedList$Entry next>;
    goto label1;
 label2:
    return l1;
}
```
5. <java.util.HashMap: java.lang.Object clone()>
```
public java.lang.Object clone() {
    java.util.HashMap l0, l1;
    java.lang.Object $stack3;
    java.util.HashMap$Entry[] $stack4, $stack6;
    int $stack5;
    java.lang.CloneNotSupportedException $stack7, l2;

    l0 := @this: java.util.HashMap;
    l1 = null;
 label1:
    $stack3 = specialinvoke l0.<java.util.AbstractMap: java.lang.Object clone()>();
    l1 = (java.util.HashMap) $stack3;
 label2:
    goto label4;
 label3:
        $stack7 := @caughtexception;
        l2 = $stack7;
 label4:
    $stack4 = l0.<java.util.HashMap: java.util.HashMap$Entry[] table>;
    $stack5 = lengthof $stack4;
    $stack6 = newarray (java.util.HashMap$Entry)[$stack5];
    l1.<java.util.HashMap: java.util.HashMap$Entry[] table> = $stack6;
    l1.<java.util.HashMap: java.util.Set entrySet> = null;
    l1.<java.util.HashMap: int modCount> = 0;
    l1.<java.util.HashMap: int size> = 0;
    virtualinvoke l1.<java.util.HashMap: void init()>();
    specialinvoke l1.<java.util.HashMap: void putAllForCreate(java.util.Map)>(l0);
    return l1;
    catch java.lang.CloneNotSupportedException from label1 to label2 with label3;
}
```
6. <javax.swing.JRootPane: javax.swing.JLayeredPane createLayeredPane()>
```
protected javax.swing.JLayeredPane createLayeredPane() {
    javax.swing.JLayeredPane $stack2, l1;
    java.lang.StringBuilder $stack3, $stack5, $stack6;
    javax.swing.JRootPane l0;
    java.lang.String $stack4, $stack7;
    l0 := @this: javax.swing.JRootPane;
    $stack2 = new javax.swing.JLayeredPane;
    specialinvoke $stack2.<javax.swing.JLayeredPane: void <init>()>();
    l1 = $stack2;
    $stack3 = new java.lang.StringBuilder;
    specialinvoke $stack3.<java.lang.StringBuilder: void <init>()>();
    $stack4 = virtualinvoke l0.<javax.swing.JRootPane: java.lang.String getName()>();
    $stack5 = virtualinvoke $stack3.<java.lang.StringBuilder: java.lang.StringBuilder append(java.lang.String)>($stack4);
    $stack6 = virtualinvoke $stack5.<java.lang.StringBuilder: java.lang.StringBuilder append(java.lang.String)>(".layeredPane");
    $stack7 = virtualinvoke $stack6.<java.lang.StringBuilder: java.lang.String toString()>();
    virtualinvoke l1.<javax.swing.JLayeredPane: void setName(java.lang.String)>($stack7);
    return l1;
}
public JRootPane() {
    setLayeredPane(createLayeredPane());
}   
public void setLayeredPane(JLayeredPane paramJLayeredPane) {
    this.layeredPane = paramJLayeredPane;
}
```
7.
