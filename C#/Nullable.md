## Nuable reference type 

we always meet the nullable exception,and Nuable reference type is born to this.

### Prerequisites
add the Nullable node in PropertyGroup node in .csproj file.
```xml
  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
    <Nullable>enable</Nullable>
  </PropertyGroup>
```
after change the .csproj file,we can use the ? annotation in our code.
``` c#
    public class Student
    {
        public int Age { get; set; }
        public string Name { get; set; }

        public Pen? pen { get; set; }

        public Student(int age,string name)
        {
            this.Age = age;
            this.Name = name;
        }
    }
```

We all know one student must have name and age,and doesn't require to have a pen.

When someone create Student entity,we ensure that the entity must have name and age.We keep our code cleaner without check if the name is null.


