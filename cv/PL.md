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
