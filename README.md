# Módulo 20
Conteudo de apoio:
# Exercicio
Em Java, uma interface funcional é uma interface que possui apenas um método abstrato. Interfaces funcionais são frequentemente utilizadas em programação funcional e são fundamentais para o funcionamento de expressões lambda e referências a métodos. Para identificar se uma interface é funcional, basta seguir as diretrizes da linguagem e usar a anotação @FunctionalInterface ou simplesmente garantir que haja apenas um método abstrato na interface. A anotação @FunctionalInterface não é obrigatória, mas ela ajuda a evitar erros, pois o compilador irá verificar se a interface atende aos requisitos.

### Exemplo: 
      @FunctionalInterface
public interface MinhaInterfaceFuncional {
    void meuMetodoAbstrato();

    // Outros métodos não abstratos (opcionais)
    default void meuMetodoPadrao() {
        System.out.println("Este é um método padrão.");
    }

    // Outros métodos não abstratos (opcionais)
    static void meuMetodoEstatico() {
        System.out.println("Este é um método estático.");
    }
}

Se remover a anotação @FunctionalInterface, o código ainda será válido desde que haja apenas um método abstrato na interface. No entanto, a anotação ajuda a documentar a intenção de que a interface é projetada para ser funcional.

É importante observar que métodos herdados da classe Object (como toString, equals e hashCode) não são contados na contagem de métodos abstratos ao determinar se uma interface é funcional. A contagem é feita apenas em relação aos métodos declarados na própria interface.
