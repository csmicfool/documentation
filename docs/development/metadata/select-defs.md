# selectDefs

Path: metadata > selectDefs > {EntityType}

Parameters used by [Select](../select-builder.md) framework that converts serarch parameters (sent from the front-end) to ORM queries.

## accessControlFilterClassNameMap

Class names for access control filters. Classes should implement `Espo\Core\Select\AccessControl\Filter` interface.

Default filters are available at `Espo\Core\Select\AccessControl\Filters`.

Note: `mandotory` filter is applied for all users. If you need to apply some a

## boolFilterClassNameMap

Class names for bool filters. Classes should implement `Espo\Core\Select\Bool\Filter` interface.

## primaryFilterClassNameMap

Class names for primary filters. Classes should implement `Espo\Core\Select\Primary\Filter` interface.

## selectAttributesDependencyMap

Selecting a specific attribute will actually select attributes defined by the map.

Example:

```json
{
    "selectAttributesDependencyMap": {
        "subject": ["name"],
        "personStringData": ["fromString", "fromEmailAddressId"]
    }
}
```

## whereItemConverterClassNameMap

Implementations for custom where items.

Example: 

```json
{
    "whereItemConverterClassNameMap": {
        "id_isOfType": "Espo\\Classes\\Select\\User\\Where\\ItemConverters\\IsOfType"
    }
}
```

Classes should implement `Espo\Core\Select\Where\ItemConverter` interface.

## accessControlFilterResolverClassName

Should implement `Espo\Core\Select\AccessControl\FilterResolver` interface.

