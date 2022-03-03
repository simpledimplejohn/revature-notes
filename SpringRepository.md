# Using the Spring Repository 

## What you can do
- It's an interface
- Annotate with @Repository
- implement JpaRepository

## Crud Methods
- Default available methods 
    - findAll()
    - findAllById()
    - findById()
    - deleteById()
    - save()
    - saveAll()
- Creating Crud methods:
    - introducer and criteria
        - introducers:
            - find
            - read
            - query
            - count 
            - get
        - limit results with
            - Top
            - Distinct
            - First 
        - criteria (whatever the object paramater name is)
            - ByName
            - ById
        - Sorting
            - OrderByName
            - OrderByNameAsc
            - OrderByPrice
