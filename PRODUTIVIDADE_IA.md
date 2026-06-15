
# Potencializando Produtividade Java com IA

Essa atividade propõe o uso de inteligências artificiais como tutores para maior fonte de aprendizado.

## Códigos

Código gerado pela IA
```bash
List<Motorista> habilitados = getMotoristasDaEmpresa().stream()
    .filter(Motorista::isCnhAtiva)
    .sorted(
        Comparator.comparingInt(
            Motorista::getAnosEmpresa
        )
    )
    .toList();
```

Código alterado para incluir o seguro
```bash
List<Motorista> habilitados = getMotoristasDaEmpresa().stream()
    .filter(Motorista::isCnhAtiva)
    .filter(m -> m.getSeguro().map(
        Seguro::isAtivo).orElse(false)
    )
    .sorted(
        Comparator.comparingInt(
            Motorista::getAnosEmpresa
        )
    )
    .toList();
```
## Relatos de Aprendizagem

O principal insight obtido foi que, com a Stream API, não é mais necessário controlar manualmente loops, listas temporárias e ordenações, basta descrever as regras de negócio em uma sequência de operações. Também aprendi que o uso de Optional torna o código mais seguro ao evitar verificações manuais de null e reduzir a chance de NullPointerException. Além disso, Method References e comparadores modernos deixam o código mais legível e fácil de manter.

## Prompts utilizados

Não usei prompts além dos que estão disponiveis na atividade, esses listados abaixo.
 - Atue como um engenheiro de software sênior especializado em Java. Tenho um código legado que usa Java 7 (for-each e Comparator anônimo) e preciso modernizá-lo para Java 21, utilizando Stream API e Method References.
 Reescreva o código, explique cada mudança realizada e por que a nova versão é mais segura e mais fácil de manter.
 - Agora, explique-me: se eu quisesse que esse filtro também removesse motoristas que não possuem um Optional de seguro ativo, como eu alteraria essa Stream? Não me dê o código, explique-me a lógica.


## Evidências

![Captura de tela - IDE + Terminal](https://i.ibb.co/chhWPm8Q/Motoristas.png)

