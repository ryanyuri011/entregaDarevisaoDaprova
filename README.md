# entregaDarevisaoDaprova

1  System.out.println("Digite o tamanho dos vetores:");
    int tamanho = scanner.nextInt();

    int[] vetor1 = new int[1];
    int[] vetor2 = new int[5];

    System.out.println("Digite os elementos do primeiro vetor:");
    preencherVetor(scanner, vetor1);

    System.out.println("Digite os elementos do segundo vetor:");
    preencherVetor(scanner, vetor2);

    int[] vetorSoma = somaDeVetores(vetor1, vetor2);
    
    System.out.println("Resultado da soma dos vetores:");
    imprimirVetor(vetorSoma);
}


// Método para preencher um vetor com valores fornecidos pelo usuário
public static void preencherVetor(Scanner scanner, int[] vetor) {
    for (int i = 0; i < vetor.length; i++) {
        vetor[i] = scanner.nextInt();
    }
}

// Método para calcular a soma de dois vetores
public static int[] somaDeVetores(int[] vetor1, int[] vetor2) {
    int[] resultado = new int[vetor1.length];
    for (int i = 0; i < vetor1.length; i++) {
        resultado[i] = vetor1[i] + vetor2[i];
    }
    return resultado;
}

// Método para imprimir um vetor
public static void imprimirVetor(int[] vetor) {
    for (int i = 0; i < vetor.length; i++) {
        System.out.print(vetor[i] + " ");
    }
    System.out.println();
}


33)public class MediaDoVetor {

public static void main(String[] args) {
    int[] vetor = {4, 8, 15, 16, 23, 42}; // Exemplo de vetor
    double media = calcularMedia(vetor); // Chamada do método que calcula a média
    imprimirMedia(media); // Imprime a média calculada
}

// Método para calcular a média dos elementos do vetor
public static double calcularMedia(int[] vetor) {
    double soma = 0;
    for (int numero : vetor) {
        soma += numero; // Soma todos os elementos do vetor
    }
    return soma / vetor.length; // Calcula a média dividindo a soma pelo número de elementos
}

// Método para imprimir a média
public static void imprimirMedia(double media) {
    System.out.println("A média dos elementos do vetor é: " + media);
}


4:Cópia de Vetor int[] vetorOriginal = {10, 20, 30, 40, 50}; // Vetor original int[] vetorCopia = copiarVetor(vetorOriginal); // Chamada do método que copia o vetor imprimirVetor(vetorCopia); // Imprime o vetor copiado }

// Método para copiar um vetor
public static int[] copiarVetor(int[] vetorOriginal) {
    int[] vetorCopia = new int[vetorOriginal.length]; // Cria um novo vetor com o mesmo tamanho do original
    for (int i = 0; i < vetorOriginal.length; i++) {
        vetorCopia[i] = vetorOriginal[i]; // Copia cada elemento do vetor original para o vetor de cópia
    }
    return vetorCopia; // Retorna o novo vetor copiado
}

// Método para imprimir o vetor
public static void imprimirVetor(int[] vetor) {
    System.out.print("Vetor copiado: ");
    for (int valor : vetor) {
        System.out.print(valor + " ");
    }
    System.out.println();
}


5:Verificar Igualdade de Vetores: int[] vetor1 = {4, 5, 6, 7, 8}; int[] vetor2 = {4, 5, 6, 7, 8}; int[] vetor3 = {8, 7, 6, 5, 4};

    boolean saoIguais1 = saoVetoresIguais(vetor1, vetor2); // Deve retornar true
    boolean saoIguais2 = saoVetoresIguais(vetor1, vetor3); // Deve retornar false

    imprimirResultado(saoIguais1, "vetor1", "vetor2");
    imprimirResultado(saoIguais2, "vetor1", "vetor3");
}

// Método que verifica se dois vetores são iguais
public static boolean saoVetoresIguais(int[] vetor1, int[] vetor2) {
    if (vetor1.length != vetor2.length) {
        return false; // Vetores com tamanhos diferentes não são iguais
    }
    for (int i = 0; i < vetor1.length; i++) {
        if (vetor1[i] != vetor2[i]) {
            return false; // Elementos diferentes encontrados na mesma posição
        }
    }
    return true; // Todos os elementos e tamanhos são iguais
}

// Método para imprimir o resultado da comparação
public static void imprimirResultado(boolean resultado, String nomeVetor1, String nomeVetor2) {
    if (resultado) {
        System.out.println("Os " + nomeVetor1 + " e " + nomeVetor2 + " são iguais.");
    } else {
        System.out.println("Os " + nomeVetor1 + " e " + nomeVetor2 + " não são iguais.");
    }
}
int[] vetor = {1, 2, 3, 4, 5, 6};  // Exemplo de vetor
 inverterVetor(vetor);  // Chama o método que inverte o vetor
 imprimirVetor(vetor);  // Imprime o vetor invertido
}


// Método para inverter o vetor public static void inverterVetor(int[] vetor) { int n = vetor.length; for (int i = 0; i < n / 2; i++) { int temp = vetor[i]; vetor[i] = vetor[n - 1 - i]; vetor[n - 1 - i] = temp; } }

// Método para imprimir o vetor public static void imprimirVetor(int[] vetor) { System.out.print("Vetor invertido: "); for (int valor : vetor) { System.out.print(valor + " "); } System.out.println(); } }
7)Contagem de Elementos Pares e Ímpares: Escreva um programa que conte e imprima a quantidade de elementos pares e ímpares em um vetor de inteiros.

  int[] vetor = {2, 3, 5, 6, 8, 9, 10, 12}; // Exemplo de vetor de inteiros
    int[] resultado = contarParesEImpares(vetor); // Chamada do método que realiza a contagem
    imprimirResultado(resultado); // Método para imprimir os resultados
}


// Método para contar pares e ímpares

public static int[] contarParesEImpares(int[] vetor) {
    int contPares = 0;
    int contImpares = 0;

    for (int numero : vetor) { // Laço para percorrer todos os elementos do vetor
        if (numero % 2 == 0) { // Condição para verificar se o número é par
            contPares++;
        } else { // Caso não seja par, é ímpar
            contImpares++;
        }
    }
    return new int[]{contPares, contImpares}; // Retorna um array com os contadores de pares e ímpares
}
// Método para imprimir o resultado da contagem
public static void imprimirResultado(int[] resultado) {
    System.out.println("Quantidade de números pares: " + resultado[0]);
    System.out.println("Quantidade de números ímpares: " + resultado[1]);
}


8)nt[] vetorOriginal = {2, 3, 5, 6, 8, 9, 10, 12}; // Exemplo de vetor int elementoParaRemover = 6; // Elemento a ser removido

    int[] vetorModificado = removerElemento(vetorOriginal, elementoParaRemover);
    imprimirVetor(vetorModificado);
}

// Método para remover um elemento específico do vetor
public static int[] removerElemento(int[] vetor, int elemento) {
    int quantidade = 0;

    // Contar quantas vezes o elemento aparece no vetor
    for (int valor : vetor) {
        if (valor == elemento) {
            quantidade++;
        }
    }

    // Criar um novo vetor sem o elemento
    int[] novoVetor = new int[vetor.length - quantidade];
    int indice = 0;

    for (int valor : vetor) {
        if (valor != elemento) {
            novoVetor[indice++] = valor;
        }
    }

    return novoVetor;
}


// Método para imprimir o vetor
public static void imprimirVetor(int[] vetor) {
    System.out.print("Vetor modificado: [");
    for (int i = 0; i < vetor.length; i++) {
        System.out.print(vetor[i]);
        if (i < vetor.length - 1) {
            System.out.print(", ");
        }
    }
    System.out.println("]");
}
}
int[] vetor = {34, 7, 23, 32, 5, 62}; // Exemplo de vetor ordenarVetor(vetor); // Chama o método que ordena o vetor imprimirVetor(vetor); // Imprime o vetor ordenado }
// Método para ordenar o vetor em ordem crescente usando Bubble Sort
public static void ordenarVetor(int[] vetor) {
    int n = vetor.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - 1 - i; j++) {
            if (vetor[j] > vetor[j + 1]) {
                // Troca elementos se eles estão na ordem errada
                int temp = vetor[j];
                vetor[j] = vetor[j + 1];
                vetor[j + 1] = temp;
            }
        }
    }
}


// Método para imprimir o vetor
public static void imprimirVetor(int[] vetor) {
    System.out.print("Vetor ordenado: ");
    for (int valor : vetor) {
        System.out.print(valor + " ");
    }
    System.out.println();
}
int[] vetor = {45, 22, 89, 30, 17, 56, 93}; // Vetor onde será feita a busca int elementoProcurado = 30; // Elemento a ser procurado no vetor

int indice = buscaSequencial(vetor, elementoProcurado); imprimirResultado(indice, elementoProcurado); }

// Método que realiza a busca sequencial
public static int buscaSequencial(int[] vetor, int elemento) {
    for (int i = 0; i < vetor.length; i++) {
        if (vetor[i] == elemento) {
            return i; // Retorna o índice do elemento encontrado
        }
    }
    return -1; // Retorna -1 se o elemento não foi encontrado
}

// Método para imprimir o resultado da busca
public static void imprimirResultado(int indice, int elemento) {
    if (indice == -1) {
        System.out.println("Elemento " + elemento + " não encontrado no vetor.");
    } else {
        System.out.println("Elemento " + elemento + " encontrado na posição: " + indice);
    }
}
