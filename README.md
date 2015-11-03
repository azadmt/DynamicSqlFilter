# DynamicSqlFilter
Use Expression Trees to Build Dynamic Queries

It has a simple usage

            var filter = PredicateBuilder.MakeFilter<Person>(p =>
                 p.Name == null ||
                    p.Age == 87 ||
                    p.Family.StartsWith("A") ||
                    p.Name == "jack" &&
                    p.Age > 10);
        }//Result is :Name is null or Age = 87 or Family like 'A%' or Name = 'jack'  or Age > 10
