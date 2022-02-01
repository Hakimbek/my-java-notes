# Streams
Stream is a new abstract layer introduced in Java 8. Using stream, you can process data in a declarative way similar to SQL statements.

## Generating Streams
With Java 8, Collection interface has two methods to generate a Stream.

### stream() − Returns a sequential stream considering collection as its source.

### parallelStream() − Returns a parallel Stream considering collection as its source.

## forEach
Stream has provided a new method ‘forEach’ to iterate each element of the stream.

## map
The ‘map’ method is used to map each element to its corresponding result.

## filter
The ‘filter’ method is used to eliminate elements based on a criteria.

## limit
The ‘limit’ method is used to reduce the size of the stream.

## sorted
The ‘sorted’ method is used to sort the stream.

```java
public class Main {
    public static void main(String[] args) {
        List<Person> people = new ArrayList<>(Arrays.asList(
           new Person("James Bond", 20, Gender.MALE),
           new Person("Alina Smith", 33, Gender.FEMALE),
           new Person("Helen Keller", 19, Gender.FEMALE),
           new Person("Boba Fett", 35, Gender.MALE),
           new Person("Harry Poter", 18, Gender.MALE),
           new Person("Dart Vader", 45 , Gender.MALE),
           new Person("Anna Cook", 7, Gender.FEMALE),
           new Person("Sia Shik", 7, Gender.FEMALE),
           new Person("Elsa Patric", 7, Gender.FEMALE),
           new Person("Hurshida Bahramova", 7, Gender.FEMALE)
        ));

        // Filter
        List<Person> females = people.stream()
                .filter(person -> person.getGender().equals(Gender.FEMALE))
                .collect(Collectors.toList());

        // Sort
        List<Person> sorted = people.stream()
                .sorted(Comparator.comparing(Person::getName).thenComparing(Person::getAge))
                .collect(Collectors.toList());

        // All match
        boolean allMatch = people.stream()
                .allMatch(person -> person.getAge() > 20);

        // Any match
        boolean anyMatch = people.stream()
                .anyMatch(person -> person.getAge() > 12);

        // None match
        boolean noneMatch = people.stream()
                .noneMatch(person -> person.getName().equals("Elsa"));

        // Max
        people.stream()
                .max(Comparator.comparing(Person::getAge)).
                ifPresent(System.out::println);

        // Min
        people.stream()
                .min(Comparator.comparing(Person::getAge)).
                ifPresent(System.out::println);

        // Group

        // By gender
        Map<Gender, List<Person>> groupByGender = people.stream()
                .collect(Collectors.groupingBy(Person::getGender));

        // By gender count
        Map<Gender, Long> genderCount = people.stream()
                .collect(Collectors.groupingBy(Person::getGender, Collectors.counting()));

        // Map
        people.stream()
                .filter(person -> person.getGender().equals(Gender.FEMALE))
                .max(Comparator.comparing(Person::getAge))
                .map(Person::getName)
                .ifPresent(System.out::println);
    }
}

```
