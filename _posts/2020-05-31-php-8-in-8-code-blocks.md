---
title: PHP 8 в 8 примерах с кодом
layout: post
original: https://stitcher.io/blog/php-8-in-8-code-blocks
---

В PHP 8 планируется много новых возможностей. В этом посте рассмотрим самые интересные из них. 

## 1. Атрибуты (или аннотации)

```php
use \Support\Attributes\ListensTo;

class ProductSubscriber
{
    <<ListensTo(ProductCreated::class)>>
    public function onProductCreated(ProductCreated $event) { /* … */ }

    <<ListensTo(ProductDeleted::class)>>
    public function onProductDeleted(ProductDeleted $event) { /* … */ }
}
```

## 2. Union types - объединенные типы. 

Это значит, что переменная может принимать один из перечисленных типов. Также вводится тип mixed, который объединяет множество типов.

```php
public function foo(Foo|Bar $input): int|float;

public function bar(mixed $input): mixed;
```

## 3. Возвращаемое значение static.

```php
interface Foo
{
    public function bar(): static;
}
```

## 4. JIT (Just In Time) или просто компиляция "на лету".

```php
[JIT]
opcache.jit=5
```

## 5. throw можно использовать в выражениях.

```php
$triggerError = fn() => throw new MyError();

$foo = $bar['offset'] ?? throw new OffsetDoesNotExist('offset');
```

## 6. Можно не указывать переменную в catch, если она не нужна.

```php
try {
    // Something goes wrong
} catch (MySpecialException) {
    Log::error("Something went wrong");
}
```

## 7. Разрешено оставлять запятую после последнего аргумента в функции.

```php
public function(
    string $parameterA,
    int $parameterB,
    Foo $objectfoo,
) {
    // …
}
```

## 8. Новые строковые функции.

```php
str_contains('string with lots of words', 'words');

str_starts_with('haystack', 'hay');

str_ends_with('haystack', 'stack');
```

Давайте не будем себя обманывать. Восемь примеров недостаточно, чтобы описать все крутые фичи в PHP 8. Добавим еще парочку.

Новый интерфейс Stringable.

```php
function bar(Stringable $stringable) { /* … */ }
```

Вызов ::class прямо на объектах.

```php
$object::class
```

Это были наиболее интересные фичи на мой взгляд. На самом деле нововведений в новой версии намного больше.

Какая из фич в новой версии PHP вам нравится больше всего?