### Learn & Android & ArrayList

容器

### 继承关系

```mermaid
graph TD
A(Iterator(接口)) --> B(Collection(接口))
A --> C(ListIterator(接口))
B --> G(AbstractCollection(接口))
B --> D(List(接口))
C --> D
D --> E(AbstractList)
E --> F(ArrayList)
B --> E
H[竖向流程图]
```

### Iterator

迭代器

```markdown
public interface Iterator<E> {

    boolean hasNext();

    E next();

    default void remove() {
        throw new UnsupportedOperationException("remove");
    }
    default void forEachRemaining(Consumer<? super E> action) {
    Objects.requireNonNull(action);
    while (hasNext())
    action.accept(next());
}
```

### [HOME](https://daixuenan.github.io/)