# Record Processor

Process record-based sources using a pipeline approach

```php
<?php
    require __DIR__ . './vendor/autoload.php';

    use RodrigoPedra\RecordProcessor\ProcessorBuilder;
    
    $processor = (new ProcessorBuilder)
        ->readFromCSVFile(__DIR__ . '/storage/input.xlsx')
        ->serializeToHTMLTable()
        ->build();
    
    $output = $processor->process();
    
    echo $output->output(), \PHP_EOL;
    
    exit;
```

## TODO

Add documentation
