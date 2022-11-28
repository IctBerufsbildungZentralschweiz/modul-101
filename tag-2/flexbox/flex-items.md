# 03 Die Flex-Items

Die folgende Liste von Eigenschaften für die Flex-Items ist nicht abschliessend, zeigt jedoch die wichtigten Elemente.

![Flex Items](../../.gitbook/assets/flex-items%20%281%29.svg)

## Flex-Items: `order`

Standardmässig befinden sich die Flex-Items in der Reihenfolge, wie sie im Code auftauchen. Mit der `order`-Eigenschaft kann man auf dieses Standardverhalten Einfluss nehmen.

Der Browser sortiert die Elemente aufsteigend, gemäss des `order` Werts.

![Order](../../.gitbook/assets/order.svg)

```css
.item {
  order: 5; /* Standard ist 0, Wert darf auch kleiner als 0 sein */
}
```

## Flex-Items: `flex-grow`

Diese Eigenschaft ermöglicht es einem Flex-Item zu wachsen, falls nötig/möglich. Der Eigenschafts-Wert muss eine einheitlose Zahl sein - es handelt sich dabei um eine Proportion. Der Wert definiert, wieviel des nicht genutzten Platzes im Flex-Container, durch das Item vereinnahmt werden sollen.

Zwei Beispiele mit drei Flex-Items auf einer Linie: 1. Hat jedes Flex-Item einen 'flex-grow'-Wert von 1, wird der nicht genutzte Platz durch drei geteilt und gleichmässig zwischen den Elementen aufgeteilt. 2. Hat ein Flex-Item einen 'flex-grow'-Wert von 2, wird der nicht genutzte Platz durch vier geteilt. Das Element mit dem Wert von 2 erhält dann 2/4 des nicht genutzten Platzes, die anderen beiden nur 1/4.

![Order](../../.gitbook/assets/flex-grow.svg)

```css
.item {
  flex-grow: <number>; /* Standard ist 0 */
}
```

## Flex-Items: `flex-shrink`

Diese Eigenschaft ermöglicht es einem Flex-Item zu schrumpfen, falls nötig.

```css
.item {
  flex-shrink: <number>; /* Standard ist 0 */
}
```

## Flex-Items: `align-self`

Die `align-self`-Eigenschaft ermöglicht es einem Flex-Item die Ausrichtung des Flex-Containers \(`align-items`\) zu überschreiben.

![Order](../../.gitbook/assets/align-self.svg)

```css
.item {
  align-self: auto; /* Oder: flex-start | flex-end | center | baseline | stretch */
}
```

