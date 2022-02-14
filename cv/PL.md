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

4-1. <java.util.AbstractCollection: java.lang.Object[] toArray()>
```
public java.lang.Object[] toArray() {
    java.util.AbstractCollection l0;
    int $stack4, $stack6, l3;
    java.lang.Object[] l1, $stack13, $stack8;
    java.util.Iterator l2;
    boolean $stack7, $stack9;
    java.lang.Object $stack10;
    l0 := @this: java.util.AbstractCollection;
    $stack4 = virtualinvoke l0.<java.util.AbstractCollection: int size()>();
    l1 = newarray (java.lang.Object)[$stack4];
    l2 = virtualinvoke l0.<java.util.AbstractCollection: java.util.Iterator iterator()>();
    $stack10 = interfaceinvoke l2.<java.util.Iterator: java.lang.Object next()>();
    l1[l3] = $stack10;
    $stack8 = l1;
    return $stack8;
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

7. <java.util.zip.ZipInputStream: void <init>(java.io.InputStream)>
```
public ZipInputStream(InputStream paramInputStream) {
    super(new PushbackInputStream(paramInputStream, 512), new Inflater(true), 512);
}
public InflaterInputStream(InputStream paramInputStream, Inflater paramInflater, int paramInt) {
    super(paramInputStream);
}
protected FilterInputStream(InputStream paramInputStream) {
    this.in = paramInputStream;
}
```

8. <org.eclipse.core.internal.resources.MarkerSet: org.eclipse.core.internal.resources.IMarkerSetElement[] elements()>    
```
public org.eclipse.core.internal.resources.IMarkerSetElement[] elements() {
    org.eclipse.core.internal.resources.MarkerSet this;
    int $stack5, $stack11, j, i, $stack7;
    org.eclipse.core.internal.resources.IMarkerSetElement[] result, $stack8, $stack6;
    org.eclipse.core.internal.resources.IMarkerSetElement element;

    this := @this: org.eclipse.core.internal.resources.MarkerSet;
    $stack5 = this.<org.eclipse.core.internal.resources.MarkerSet: int elementCount>;
    result = newarray (org.eclipse.core.internal.resources.IMarkerSetElement)[$stack5];
    j = 0;
    i = 0;
    goto label3;
 label1:
    $stack8 = this.<org.eclipse.core.internal.resources.MarkerSet: org.eclipse.core.internal.resources.IMarkerSetElement[] elements>;
    element = $stack8[i];
    if element == null goto label2;
    $stack11 = j;
    j = j + 1;
    result[$stack11] = element;
 label2:
    i = i + 1;
 label3:
    $stack6 = this.<org.eclipse.core.internal.resources.MarkerSet: org.eclipse.core.internal.resources.IMarkerSetElement[] elements>;
    $stack7 = lengthof $stack6;
    if i < $stack7 goto label1;
    return result;
}    
```

9. <org.eclipse.debug.internal.core.ListenerList: java.lang.Object[] getListeners()>
```
public synchronized java.lang.Object[] getListeners() {
    org.eclipse.debug.internal.core.ListenerList this;
    int $stack2, $stack3, $stack4;
    java.lang.Object[] result, $stack5, $stack6;
    java.lang.Object nativeArrayCopy7;

    this := @this: org.eclipse.debug.internal.core.ListenerList;
    $stack2 = this.<org.eclipse.debug.internal.core.ListenerList: int fSize>;
    if $stack2 != 0 goto label1;
    $stack6 = <org.eclipse.debug.internal.core.ListenerList: java.lang.Object[] EmptyArray>;
    return $stack6;
 label1:
    $stack3 = this.<org.eclipse.debug.internal.core.ListenerList: int fSize>;
    result = newarray (java.lang.Object)[$stack3];
    $stack5 = this.<org.eclipse.debug.internal.core.ListenerList: java.lang.Object[] fListeners>;
    $stack4 = this.<org.eclipse.debug.internal.core.ListenerList: int fSize>;
    staticinvoke <java.lang.System: void arraycopy(java.lang.Object,int,java.lang.Object,int,int)>($stack5, 0, result, 0, $stack4);
    nativeArrayCopy7 = $stack5[0];
    result[0] = nativeArrayCopy7;
    return result;
}
```

10．<java.util.Hashtable: java.util.Collection values()>
```
public java.util.Collection values() {
    java.util.Hashtable l0;
    java.util.Collection $stack1, $stack2, $stack4;
    java.util.Hashtable$ValueCollection $stack3;
    l0 := @this: java.util.Hashtable;
    $stack1 = l0.<java.util.Hashtable: java.util.Collection values>;
    if $stack1 != null goto label1;
    $stack3 = new java.util.Hashtable$ValueCollection;
    specialinvoke $stack3.<java.util.Hashtable$ValueCollection: void <init>(java.util.Hashtable,java.util.Hashtable$1)>(l0, null);
    $stack4 = staticinvoke <java.util.Collections: java.util.Collection synchronizedCollection(java.util.Collection,java.lang.Object)>($stack3, l0);
    l0.<java.util.Hashtable: java.util.Collection values> = $stack4;
 label1:
    $stack2 = l0.<java.util.Hashtable: java.util.Collection values>;
    return $stack2;
}    
```

11. <java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$1: java.util.Map$Entry next()>
    
```
public java.util.Map$Entry next() {
    java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$UnmodifiableEntry $stack1;
    java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$1 l0;
    java.util.Iterator $stack2;
    java.lang.Object $stack3;
    java.util.Map$Entry $stack4;

    l0 := @this: java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$1;
    $stack1 = new java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$UnmodifiableEntry;
    $stack2 = l0.<java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$1: java.util.Iterator i>;
    $stack3 = interfaceinvoke $stack2.<java.util.Iterator: java.lang.Object next()>();
    $stack4 = (java.util.Map$Entry) $stack3;
    specialinvoke $stack1.<java.util.Collections$UnmodifiableMap$UnmodifiableEntrySet$UnmodifiableEntry: void <init>(java.util.Map$Entry)>($stack4);
    return $stack1;
}
```    
# In static methods
12. <java.util.Arrays: java.util.List asList(java.lang.Object[])>
```
public static transient java.util.List asList(java.lang.Object[]) {
    java.util.Arrays$ArrayList $stack1;
    java.lang.Object[] l0;
    l0 := @parameter0: java.lang.Object[];
    $stack1 = new java.util.Arrays$ArrayList;
    specialinvoke $stack1.<java.util.Arrays$ArrayList: void <init>(java.lang.Object[])>(l0);
    return $stack1;
}
void <init>(java.lang.Object[]) {
    java.util.Arrays$ArrayList l0;
    java.lang.Object[] l1;
    java.lang.NullPointerException $stack2;
    l0 := @this: java.util.Arrays$ArrayList;
    l1 := @parameter0: java.lang.Object[];
    specialinvoke l0.<java.util.AbstractList: void <init>()>();
    if l1 != null goto label1;
    $stack2 = new java.lang.NullPointerException;
    specialinvoke $stack2.<java.lang.NullPointerException: void <init>()>();
    throw $stack2;
 label1:
    l0.<java.util.Arrays$ArrayList: java.lang.Object[] a> = l1;
    return;
}
```
13. <java.util.Arrays: java.lang.Object[] copyOf(java.lang.Object[],int,java.lang.Class)>
```
public static java.lang.Object[] copyOf(java.lang.Object[], int, java.lang.Class) {
    java.lang.Class l2, $stack4;
    int l1, $stack7, $stack10;
    java.lang.Object $stack5, nativeArrayCopy11;
    java.lang.Object[] $stack6, l3, l0, $stack11, $stack12;
    l0 := @parameter0: java.lang.Object[];
    l1 := @parameter1: int;
    l2 := @parameter2: java.lang.Class;
    if l2 != class "[Ljava/lang/Object;" goto label1;
    $stack11 = newarray (java.lang.Object)[l1];
    $stack12 = (java.lang.Object[]) $stack11;
    goto label2;
 label1:
    $stack4 = virtualinvoke l2.<java.lang.Class: java.lang.Class getComponentType()>();
    $stack5 = staticinvoke <java.lang.reflect.Array: java.lang.Object newInstance(java.lang.Class,int)>($stack4, l1);
    $stack5 = newarray (java.lang.String)[1];
    $stack5 = newarray (sun.security.jca.ProviderConfig)[1];
    $stack6 = (java.lang.Object[]) $stack5;
    $stack12 = (java.lang.Object[]) $stack6;
 label2:
    l3 = $stack12;
    $stack7 = lengthof l0;
    $stack10 = staticinvoke <java.lang.Math: int min(int,int)>($stack7, l1);
    staticinvoke <java.lang.System: void arraycopy(java.lang.Object,int,java.lang.Object,int,int)>(l0, 0, l3, 0, $stack10);
    l3[0] = nativeArrayCopy11;
    nativeArrayCopy11 = l0[0];
    return l3;
}  
```
14. <java.util.Collections: java.util.Set synchronizedSet(java.util.Set,java.lang.Object)>     
```
static java.util.Set synchronizedSet(java.util.Set, java.lang.Object) {
    java.util.Collections$SynchronizedSet $stack2;
    java.util.Set l0;
    java.lang.Object l1;
    l0 := @parameter0: java.util.Set;
    l1 := @parameter1: java.lang.Object;
    $stack2 = new java.util.Collections$SynchronizedSet;
    specialinvoke $stack2.<java.util.Collections$SynchronizedSet: void <init>(java.util.Set,java.lang.Object)>(l0, l1);
    return $stack2;
}
void <init>(java.util.Set, java.lang.Object) {
    java.util.Collections$SynchronizedSet l0;
    java.util.Set l1;
    java.lang.Object l2;
    l0 := @this: java.util.Collections$SynchronizedSet;
    l1 := @parameter0: java.util.Set;
    l2 := @parameter1: java.lang.Object;
    specialinvoke l0.<java.util.Collections$SynchronizedCollection: void <init>(java.util.Collection,java.lang.Object)>(l1, l2);
    return;
}
void <init>(java.util.Collection, java.lang.Object) {
    java.util.Collections$SynchronizedCollection l0;
    java.util.Collection l1;
    java.lang.Object l2;
    l0 := @this: java.util.Collections$SynchronizedCollection;
    l1 := @parameter0: java.util.Collection;
    l2 := @parameter1: java.lang.Object;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    l0.<java.util.Collections$SynchronizedCollection: java.util.Collection c> = l1;
    l0.<java.util.Collections$SynchronizedCollection: java.lang.Object mutex> = l2;
    return;
}
```
15. <java.util.Collections: java.util.Map unmodifiableMap(java.util.Map)>
```
public static java.util.Map unmodifiableMap(java.util.Map) {
    java.util.Collections$UnmodifiableMap $stack1;
    java.util.Map l0;
    l0 := @parameter0: java.util.Map;
    $stack1 = new java.util.Collections$UnmodifiableMap;
    specialinvoke $stack1.<java.util.Collections$UnmodifiableMap: void <init>(java.util.Map)>(l0);
    return $stack1;
}
void <init>(java.util.Map) {
    java.util.Collections$UnmodifiableMap l0;
    java.util.Map l1;
    java.lang.NullPointerException $stack2;
    l0 := @this: java.util.Collections$UnmodifiableMap;
    l1 := @parameter0: java.util.Map;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    l0.<java.util.Collections$UnmodifiableMap: java.util.Set keySet> = null;
    l0.<java.util.Collections$UnmodifiableMap: java.util.Set entrySet> = null;
    l0.<java.util.Collections$UnmodifiableMap: java.util.Collection values> = null;
    if l1 != null goto label1;
    $stack2 = new java.lang.NullPointerException;
    specialinvoke $stack2.<java.lang.NullPointerException: void <init>()>();
    throw $stack2;
 label1:
    l0.<java.util.Collections$UnmodifiableMap: java.util.Map m> = l1;
    return;
}
```   
16. <java.util.Collections: java.util.Set unmodifiableSet(java.util.Set)>
```
public static java.util.Set unmodifiableSet(java.util.Set) {
    java.util.Collections$UnmodifiableSet $stack1;
    java.util.Set l0;
    l0 := @parameter0: java.util.Set;
    $stack1 = new java.util.Collections$UnmodifiableSet;
    specialinvoke $stack1.<java.util.Collections$UnmodifiableSet: void <init>(java.util.Set)>(l0);
    return $stack1;
}
void <init>(java.util.Set) {
    java.util.Collections$UnmodifiableSet l0;
    java.util.Set l1;
    l0 := @this: java.util.Collections$UnmodifiableSet;
    l1 := @parameter0: java.util.Set;
    specialinvoke l0.<java.util.Collections$UnmodifiableCollection: void <init>(java.util.Collection)>(l1);
    return;
}
void <init>(java.util.Collection) {
    java.util.Collections$UnmodifiableCollection l0;
    java.util.Collection l1;
    java.lang.NullPointerException $stack2;
    l0 := @this: java.util.Collections$UnmodifiableCollection;
    l1 := @parameter0: java.util.Collection;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    if l1 != null goto label1;
    $stack2 = new java.lang.NullPointerException;
    specialinvoke $stack2.<java.lang.NullPointerException: void <init>()>();
    throw $stack2;
 label1:
    l0.<java.util.Collections$UnmodifiableCollection: java.util.Collection c> = l1;
    return;
}
```   
17. <java.util.Collections: java.util.Map synchronizedMap(java.util.Map)>
```
public static java.util.Map synchronizedMap(java.util.Map){
    java.util.Collections$SynchronizedMap $stack1;
    java.util.Map l0;
    l0 := @parameter0: java.util.Map;
    $stack1 = new java.util.Collections$SynchronizedMap;
    specialinvoke $stack1.<java.util.Collections$SynchronizedMap: void <init>(java.util.Map)>(l0);
    return $stack1;
}
void <init>(java.util.Map) {
    java.util.Collections$SynchronizedMap l0;
    java.util.Map l1;
    java.lang.NullPointerException $stack2;
    l0 := @this: java.util.Collections$SynchronizedMap;
    l1 := @parameter0: java.util.Map;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    l0.<java.util.Collections$SynchronizedMap: java.util.Set keySet> = null;
    l0.<java.util.Collections$SynchronizedMap: java.util.Set entrySet> = null;
    l0.<java.util.Collections$SynchronizedMap: java.util.Collection values> = null;
    if l1 != null goto label1;
    $stack2 = new java.lang.NullPointerException;
    specialinvoke $stack2.<java.lang.NullPointerException: void <init>()>();
    throw $stack2;
 label1:
    l0.<java.util.Collections$SynchronizedMap: java.util.Map m> = l1;
    l0.<java.util.Collections$SynchronizedMap: java.lang.Object mutex> = l0;
    return;
}
```
18. <sun.nio.cs.StreamDecoder: sun.nio.cs.StreamDecoder forInputStreamReader(java.io.InputStream,java.lang.Object,java.lang.String)>     
```
public static sun.nio.cs.StreamDecoder forInputStreamReader(java.io.InputStream, java.lang.Object, java.lang.String) throws java.io.UnsupportedEncodingException {
    java.lang.String l2, l3;
    boolean $stack5;
    sun.nio.cs.StreamDecoder $stack7;
    java.io.InputStream l0;
    java.lang.Object l1;
    java.nio.charset.Charset $stack8, $stack9;
    l0 := @parameter0: java.io.InputStream;
    l1 := @parameter1: java.lang.Object;
    l2 := @parameter2: java.lang.String;
    l3 = l2;
    $stack9 = staticinvoke <java.nio.charset.Charset: java.nio.charset.Charset defaultCharset()>();
    l3 = virtualinvoke $stack9.<java.nio.charset.Charset: java.lang.String name()>();
 label1:
    $stack5 = staticinvoke <java.nio.charset.Charset: boolean isSupported(java.lang.String)>(l3);
    if $stack5 == 0 goto label3;
    $stack7 = new sun.nio.cs.StreamDecoder;
    $stack8 = staticinvoke <java.nio.charset.Charset: java.nio.charset.Charset forName(java.lang.String)>(l3);
    specialinvoke $stack7.<sun.nio.cs.StreamDecoder: void <init>(java.io.InputStream,java.lang.Object,java.nio.charset.Charset)>(l0, l1, $stack8);
 label2:
    return $stack7;
}
void <init>(java.io.InputStream, java.lang.Object, java.nio.charset.Charset) {
    sun.nio.cs.StreamDecoder l0;
    java.io.InputStream l1;
    java.lang.Object l2;
    java.nio.charset.Charset l3;
    java.nio.charset.CharsetDecoder $stack4, $stack6, $stack8;
    java.nio.charset.CodingErrorAction $stack5, $stack7;
    l0 := @this: sun.nio.cs.StreamDecoder;
    l1 := @parameter0: java.io.InputStream;
    l2 := @parameter1: java.lang.Object;
    l3 := @parameter2: java.nio.charset.Charset;
    $stack4 = virtualinvoke l3.<java.nio.charset.Charset: java.nio.charset.CharsetDecoder newDecoder()>();
    $stack5 = <java.nio.charset.CodingErrorAction: java.nio.charset.CodingErrorAction REPLACE>;
    $stack6 = virtualinvoke $stack4.<java.nio.charset.CharsetDecoder: java.nio.charset.CharsetDecoder onMalformedInput(java.nio.charset.CodingErrorAction)>($stack5);
    $stack7 = <java.nio.charset.CodingErrorAction: java.nio.charset.CodingErrorAction REPLACE>;
    $stack8 = virtualinvoke $stack6.<java.nio.charset.CharsetDecoder: java.nio.charset.CharsetDecoder onUnmappableCharacter(java.nio.charset.CodingErrorAction)>($stack7);
    specialinvoke l0.<sun.nio.cs.StreamDecoder: void <init>(java.io.InputStream,java.lang.Object,java.nio.charset.CharsetDecoder)>(l1, l2, $stack8);
    return;
}
void <init>(java.io.InputStream, java.lang.Object, java.nio.charset.CharsetDecoder) {
    sun.nio.cs.StreamDecoder l0;
    java.lang.Object l2;
    java.nio.charset.CharsetDecoder l3;
    java.nio.charset.Charset $stack4;
    java.nio.channels.ReadableByteChannel $stack5;
    java.nio.ByteBuffer $stack6, $stack8;
    java.io.InputStream l1;
    l0 := @this: sun.nio.cs.StreamDecoder;
    l1 := @parameter0: java.io.InputStream;
    l2 := @parameter1: java.lang.Object;
    l3 := @parameter2: java.nio.charset.CharsetDecoder;
    specialinvoke l0.<java.io.Reader: void <init>(java.lang.Object)>(l2);
    $stack4 = virtualinvoke l3.<java.nio.charset.CharsetDecoder: java.nio.charset.Charset charset()>();
    l0.<sun.nio.cs.StreamDecoder: java.nio.charset.Charset cs> = $stack4;
    l0.<sun.nio.cs.StreamDecoder: java.nio.charset.CharsetDecoder decoder> = l3;
    $stack5 = l0.<sun.nio.cs.StreamDecoder: java.nio.channels.ReadableByteChannel ch>;
    if $stack5 != null goto label1;
    l0.<sun.nio.cs.StreamDecoder: java.io.InputStream in> = l1;
    l0.<sun.nio.cs.StreamDecoder: java.nio.channels.ReadableByteChannel ch> = null;
    $stack8 = staticinvoke <java.nio.ByteBuffer: java.nio.ByteBuffer allocate(int)>(8192);
    l0.<sun.nio.cs.StreamDecoder: java.nio.ByteBuffer bb> = $stack8;
 label1:
    $stack6 = l0.<sun.nio.cs.StreamDecoder: java.nio.ByteBuffer bb>;
    virtualinvoke $stack6.<java.nio.ByteBuffer: java.nio.Buffer flip()>();
    return;
}
```
19. <sun.nio.cs.StreamEncoder: sun.nio.cs.StreamEncoder forOutputStreamWriter(java.io.OutputStream,java.lang.Object,java.lang.String)>  
```
public static sun.nio.cs.StreamEncoder forOutputStreamWriter(java.io.OutputStream, java.lang.Object, java.lang.String){
    java.lang.String l2, l3;
    sun.nio.cs.StreamEncoder $stack7;
    java.io.OutputStream l0;
    java.lang.Object l1;
    java.nio.charset.Charset $stack8, $stack9;
    l0 := @parameter0: java.io.OutputStream;
    l1 := @parameter1: java.lang.Object;
    l2 := @parameter2: java.lang.String;
    l3 = l2;
    if l3 != null goto label1;
    $stack9 = staticinvoke <java.nio.charset.Charset: java.nio.charset.Charset defaultCharset()>();
    l3 = virtualinvoke $stack9.<java.nio.charset.Charset: java.lang.String name()>();
 label1:
    $stack5 = staticinvoke <java.nio.charset.Charset: boolean isSupported(java.lang.String)>(l3);
    if $stack5 == 0 goto label3;
    $stack7 = new sun.nio.cs.StreamEncoder;
    $stack8 = staticinvoke <java.nio.charset.Charset: java.nio.charset.Charset forName(java.lang.String)>(l3);
    specialinvoke $stack7.<sun.nio.cs.StreamEncoder: void <init>(java.io.OutputStream,java.lang.Object,java.nio.charset.Charset)>(l0, l1, $stack8);
 label2:
    return $stack7;
}
private void <init>(java.io.OutputStream, java.lang.Object, java.nio.charset.Charset) {
    sun.nio.cs.StreamEncoder l0;
    java.io.OutputStream l1;
    java.lang.Object l2;
    java.nio.charset.Charset l3;
    java.nio.charset.CharsetEncoder $stack4, $stack6, $stack8;
    java.nio.charset.CodingErrorAction $stack5, $stack7;
    l0 := @this: sun.nio.cs.StreamEncoder;
    l1 := @parameter0: java.io.OutputStream;
    l2 := @parameter1: java.lang.Object;
    l3 := @parameter2: java.nio.charset.Charset;
    $stack4 = virtualinvoke l3.<java.nio.charset.Charset: java.nio.charset.CharsetEncoder newEncoder()>();
    $stack5 = <java.nio.charset.CodingErrorAction: java.nio.charset.CodingErrorAction REPLACE>;
    $stack6 = virtualinvoke $stack4.<java.nio.charset.CharsetEncoder: java.nio.charset.CharsetEncoder onMalformedInput(java.nio.charset.CodingErrorAction)>($stack5);
    $stack7 = <java.nio.charset.CodingErrorAction: java.nio.charset.CodingErrorAction REPLACE>;
    $stack8 = virtualinvoke $stack6.<java.nio.charset.CharsetEncoder: java.nio.charset.CharsetEncoder onUnmappableCharacter(java.nio.charset.CodingErrorAction)>($stack7);
    specialinvoke l0.<sun.nio.cs.StreamEncoder: void <init>(java.io.OutputStream,java.lang.Object,java.nio.charset.CharsetEncoder)>(l1, l2, $stack8);
    return;
}
private void <init>(java.io.OutputStream, java.lang.Object, java.nio.charset.CharsetEncoder) {
    sun.nio.cs.StreamEncoder l0;
    java.lang.Object l2;
    java.io.OutputStream l1;
    java.nio.charset.CharsetEncoder l3;
    java.nio.charset.Charset $stack4;
    java.nio.channels.WritableByteChannel $stack5;
    java.nio.ByteBuffer $stack6;
    l0 := @this: sun.nio.cs.StreamEncoder;
    l1 := @parameter0: java.io.OutputStream;
    l2 := @parameter1: java.lang.Object;
    l3 := @parameter2: java.nio.charset.CharsetEncoder;
    specialinvoke l0.<java.io.Writer: void <init>(java.lang.Object)>(l2);
    l0.<sun.nio.cs.StreamEncoder: boolean isOpen> = 1;
    l0.<sun.nio.cs.StreamEncoder: boolean haveLeftoverChar> = 0;
    l0.<sun.nio.cs.StreamEncoder: java.nio.CharBuffer lcb> = null;
    l0.<sun.nio.cs.StreamEncoder: java.io.OutputStream out> = l1;
    l0.<sun.nio.cs.StreamEncoder: java.nio.channels.WritableByteChannel ch> = null;
    $stack4 = virtualinvoke l3.<java.nio.charset.CharsetEncoder: java.nio.charset.Charset charset()>();
    l0.<sun.nio.cs.StreamEncoder: java.nio.charset.Charset cs> = $stack4;
    l0.<sun.nio.cs.StreamEncoder: java.nio.charset.CharsetEncoder encoder> = l3;
    $stack5 = l0.<sun.nio.cs.StreamEncoder: java.nio.channels.WritableByteChannel ch>;
    if $stack5 != null goto label1;
    $stack6 = staticinvoke <java.nio.ByteBuffer: java.nio.ByteBuffer allocate(int)>(8192);
    l0.<sun.nio.cs.StreamEncoder: java.nio.ByteBuffer bb> = $stack6;
 label1:
    return;
}    
```
20. <java.beans.FeatureDescriptor: java.lang.ref.Reference createReference(java.lang.Object,boolean)>
```
static java.lang.ref.Reference createReference(java.lang.Object, boolean){
    java.lang.Object l0;
    boolean l1;
    java.lang.ref.WeakReference $stack3;
    java.lang.ref.SoftReference $stack5;
    java.lang.ref.Reference l2;
    l0 := @parameter0: java.lang.Object;
    l1 := @parameter1: boolean;
    l2 = null;
    if l0 == null goto label2;
    if l1 == 0 goto label1;
    $stack5 = new java.lang.ref.SoftReference;
    specialinvoke $stack5.<java.lang.ref.SoftReference: void <init>(java.lang.Object)>(l0);
    l2 = $stack5;
    goto label2;
 label1:
    $stack3 = new java.lang.ref.WeakReference;
    specialinvoke $stack3.<java.lang.ref.WeakReference: void <init>(java.lang.Object)>(l0);
    l2 = $stack3;
 label2:
    return l2;
}
public void <init>(java.lang.Object) {
    java.lang.ref.WeakReference l0;
    java.lang.Object l1;
    l0 := @this: java.lang.ref.WeakReference;
    l1 := @parameter0: java.lang.Object;
    specialinvoke l0.<java.lang.ref.Reference: void <init>(java.lang.Object)>(l1);
    return;
}
public void <init>(java.lang.Object) {
    java.lang.ref.SoftReference l0;
    java.lang.Object l1;
    long $stack2;
    l0 := @this: java.lang.ref.SoftReference;
    l1 := @parameter0: java.lang.Object;
    specialinvoke l0.<java.lang.ref.Reference: void <init>(java.lang.Object)>(l1);
    $stack2 = <java.lang.ref.SoftReference: long clock>;
    l0.<java.lang.ref.SoftReference: long timestamp> = $stack2;
    return;
}
void <init>(java.lang.Object) {
    java.lang.ref.Reference l0;
    java.lang.Object l1;
    l0 := @this: java.lang.ref.Reference;
    l1 := @parameter0: java.lang.Object;
    specialinvoke l0.<java.lang.ref.Reference: void <init>(java.lang.Object,java.lang.ref.ReferenceQueue)>(l1, null);
    return;
}
void <init>(java.lang.Object, java.lang.ref.ReferenceQueue) {
    java.lang.ref.Reference l0;
    java.lang.Object l1;
    java.lang.ref.ReferenceQueue l2, $stack3;
    l0 := @this: java.lang.ref.Reference;
    l1 := @parameter0: java.lang.Object;
    l2 := @parameter1: java.lang.ref.ReferenceQueue;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    l0.<java.lang.ref.Reference: java.lang.Object referent> = l1;
    if l2 != null goto label1;
    $stack3 = <java.lang.ref.ReferenceQueue: java.lang.ref.ReferenceQueue NULL>;
    goto label2;
 label1:
    $stack3 = l2;
 label2:
    l0.<java.lang.ref.Reference: java.lang.ref.ReferenceQueue queue> = $stack3;
    return;
}
```
21. <java.util.Collections: java.util.Collection unmodifiableCollection(java.util.Collection)>
```
public static java.util.Collection unmodifiableCollection(java.util.Collection) {
    java.util.Collections$UnmodifiableCollection $stack1;
    java.util.Collection l0;
    l0 := @parameter0: java.util.Collection;
    $stack1 = new java.util.Collections$UnmodifiableCollection;
    specialinvoke $stack1.<java.util.Collections$UnmodifiableCollection: void <init>(java.util.Collection)>(l0);
    return $stack1;
}
void <init>(java.util.Collection) {
    java.util.Collections$UnmodifiableCollection l0;
    java.util.Collection l1;
    java.lang.NullPointerException $stack2;
    l0 := @this: java.util.Collections$UnmodifiableCollection;
    l1 := @parameter0: java.util.Collection;
    specialinvoke l0.<java.lang.Object: void <init>()>();
    if l1 != null goto label1;
    $stack2 = new java.lang.NullPointerException;
    specialinvoke $stack2.<java.lang.NullPointerException: void <init>()>();
    throw $stack2;
 label1:
    l0.<java.util.Collections$UnmodifiableCollection: java.util.Collection c> = l1;
    return;
}
```
22. <com.google.common.collect.Maps: java.util.Map$Entry immutableEntry(java.lang.Object,java.lang.Object)>   
```
public static java.util.Map$Entry immutableEntry(java.lang.Object, java.lang.Object) {
    com.google.common.collect.ImmutableEntry $stack2;
    java.lang.Object key, value;
    key := @parameter0: java.lang.Object;
    value := @parameter1: java.lang.Object;
    $stack2 = new com.google.common.collect.ImmutableEntry;
    specialinvoke $stack2.<com.google.common.collect.ImmutableEntry: void <init>(java.lang.Object,java.lang.Object)>(key, value);
    return $stack2;
}
void <init>(java.lang.Object, java.lang.Object) {
    com.google.common.collect.ImmutableEntry this;
    java.lang.Object key, value;
    this := @this: com.google.common.collect.ImmutableEntry;
    key := @parameter0: java.lang.Object;
    value := @parameter1: java.lang.Object;
    specialinvoke this.<com.google.common.collect.AbstractMapEntry: void <init>()>();
    this.<com.google.common.collect.ImmutableEntry: java.lang.Object key> = key;
    this.<com.google.common.collect.ImmutableEntry: java.lang.Object value> = value;
    return;
}
```
23. <com.google.common.collect.ImmutableList: com.google.common.collect.ImmutableList asImmutableList(java.lang.Object[])>
```
static com.google.common.collect.ImmutableList asImmutableList(java.lang.Object[]) {
    java.lang.Object[] elements;
    int $stack2;
    com.google.common.collect.SingletonImmutableList $stack3, list;
    java.lang.Object $stack4;
    com.google.common.collect.ImmutableList $stack5, $stack6;
    elements := @parameter0: java.lang.Object[];
    $stack2 = lengthof elements;
    lookupswitch($stack2)
    {
        case 0: goto label1;
        case 1: goto label2;
        default: goto label3;
    };
 label1:
    $stack5 = staticinvoke <com.google.common.collect.ImmutableList: com.google.common.collect.ImmutableList of()>();
    return $stack5;
 label2:
    $stack3 = new com.google.common.collect.SingletonImmutableList;
    $stack4 = elements[0];
    specialinvoke $stack3.<com.google.common.collect.SingletonImmutableList: void <init>(java.lang.Object)>($stack4);
    list = $stack3;
    return list;
 label3:
    $stack6 = staticinvoke <com.google.common.collect.ImmutableList: com.google.common.collect.ImmutableList construct(java.lang.Object[])>(elements);
    return $stack6;
}
void <init>(java.lang.Object) {
    com.google.common.collect.SingletonImmutableList this;
    java.lang.Object element, $stack2;
    this := @this: com.google.common.collect.SingletonImmutableList;
    element := @parameter0: java.lang.Object;
    specialinvoke this.<com.google.common.collect.ImmutableList: void <init>()>();
    $stack2 = staticinvoke <com.google.common.base.Preconditions: java.lang.Object checkNotNull(java.lang.Object)>(element);
    this.<com.google.common.collect.SingletonImmutableList: java.lang.Object element> = $stack2;
    return;
}
public static java.lang.Object checkNotNull(java.lang.Object){
    java.lang.Object reference;
    java.lang.NullPointerException $stack1;
    reference := @parameter0: java.lang.Object;
    if reference != null goto label1;
    $stack1 = new java.lang.NullPointerException;
    specialinvoke $stack1.<java.lang.NullPointerException: void <init>()>();
    throw $stack1;
 label1:
    return reference;
}
``` 
24. <com.google.common.collect.ImmutableList: com.google.common.collect.ImmutableList construct(java.lang.Object[])>
```
private static transient com.google.common.collect.ImmutableList construct(java.lang.Object[]) {
    java.lang.Object[] elements;
    int $stack2, i;
    com.google.common.collect.RegularImmutableList $stack3;
    java.lang.Object $stack4;
    elements := @parameter0: java.lang.Object[];
    i = 0;
 label1:
    $stack2 = lengthof elements;
    if i >= $stack2 goto label2;
    $stack4 = elements[i];
    staticinvoke <com.google.common.collect.ObjectArrays: java.lang.Object checkElementNotNull(java.lang.Object,int)>($stack4, i);
    i = i + 1;
    goto label1;
 label2:
    $stack3 = new com.google.common.collect.RegularImmutableList;
    specialinvoke $stack3.<com.google.common.collect.RegularImmutableList: void <init>(java.lang.Object[])>(elements);
    return $stack3;
}
void <init>(java.lang.Object[]) {
    com.google.common.collect.RegularImmutableList this;
    java.lang.Object[] array;
    int $stack2;
    this := @this: com.google.common.collect.RegularImmutableList;
    array := @parameter0: java.lang.Object[];
    $stack2 = lengthof array;
    specialinvoke this.<com.google.common.collect.RegularImmutableList: void <init>(java.lang.Object[],int,int)>(array, 0, $stack2);
    return;
}
void <init>(java.lang.Object[], int, int) {
    com.google.common.collect.RegularImmutableList this;
    int offset, size;
    java.lang.Object[] array;
    this := @this: com.google.common.collect.RegularImmutableList;
    array := @parameter0: java.lang.Object[];
    offset := @parameter1: int;
    size := @parameter2: int;
    specialinvoke this.<com.google.common.collect.ImmutableList: void <init>()>();
    this.<com.google.common.collect.RegularImmutableList: int offset> = offset;
    this.<com.google.common.collect.RegularImmutableList: int size> = size;
    this.<com.google.common.collect.RegularImmutableList: java.lang.Object[] array> = array;
    return;
}
```
25. <com.google.common.collect.RegularImmutableMap: com.google.common.collect.RegularImmutableMap$LinkedEntry newLinkedEntry(java.lang.Object,java.lang.Object,com.google.common.collect.RegularImmutableMap$LinkedEntry)>
```
private static com.google.common.collect.RegularImmutableMap$LinkedEntry newLinkedEntry(java.lang.Object, java.lang.Object, com.google.common.collect.RegularImmutableMap$LinkedEntry) {
    com.google.common.collect.RegularImmutableMap$LinkedEntry next, $stack3;
    java.lang.Object key, value;
    com.google.common.collect.RegularImmutableMap$TerminalEntry $u0;
    com.google.common.collect.RegularImmutableMap$NonTerminalEntry $u1;
    key := @parameter0: java.lang.Object;
    value := @parameter1: java.lang.Object;
    next := @parameter2: com.google.common.collect.RegularImmutableMap$LinkedEntry;
    if next != null goto label1;
    $u0 = new com.google.common.collect.RegularImmutableMap$TerminalEntry;
    $stack3 = $u0;
    specialinvoke $u0.<com.google.common.collect.RegularImmutableMap$TerminalEntry: void <init>(java.lang.Object,java.lang.Object)>(key, value);
    goto label2;
 label1:
    $u1 = new com.google.common.collect.RegularImmutableMap$NonTerminalEntry;
    $stack3 = $u1;
    specialinvoke $u1.<com.google.common.collect.RegularImmutableMap$NonTerminalEntry: void <init>(java.lang.Object,java.lang.Object,com.google.common.collect.RegularImmutableMap$LinkedEntry)>(key, value, next);
 label2:
    return $stack3;
}
void <init>(java.lang.Object, java.lang.Object, com.google.common.collect.RegularImmutableMap$LinkedEntry) {
    com.google.common.collect.RegularImmutableMap$NonTerminalEntry this;
    java.lang.Object key, value;
    com.google.common.collect.RegularImmutableMap$LinkedEntry next;
    this := @this: com.google.common.collect.RegularImmutableMap$NonTerminalEntry;
    key := @parameter0: java.lang.Object;
    value := @parameter1: java.lang.Object;
    next := @parameter2: com.google.common.collect.RegularImmutableMap$LinkedEntry;
    specialinvoke this.<com.google.common.collect.ImmutableEntry: void <init>(java.lang.Object,java.lang.Object)>(key, value);
    this.<com.google.common.collect.RegularImmutableMap$NonTerminalEntry: com.google.common.collect.RegularImmutableMap$LinkedEntry next> = next;
    return;
}
void <init>(java.lang.Object, java.lang.Object) {
    com.google.common.collect.ImmutableEntry this;
    java.lang.Object key, value;
    this := @this: com.google.common.collect.ImmutableEntry;
    key := @parameter0: java.lang.Object;
    value := @parameter1: java.lang.Object;
    specialinvoke this.<com.google.common.collect.AbstractMapEntry: void <init>()>();
    this.<com.google.common.collect.ImmutableEntry: java.lang.Object key> = key;
    this.<com.google.common.collect.ImmutableEntry: java.lang.Object value> = value;
    return;
}
void <init>(java.lang.Object, java.lang.Object) {
    com.google.common.collect.RegularImmutableMap$TerminalEntry this;
    java.lang.Object key, value;
    this := @this: com.google.common.collect.RegularImmutableMap$TerminalEntry;
    key := @parameter0: java.lang.Object;
    value := @parameter1: java.lang.Object;
    specialinvoke this.<com.google.common.collect.ImmutableEntry: void <init>(java.lang.Object,java.lang.Object)>(key, value);
    return;
}
```    
