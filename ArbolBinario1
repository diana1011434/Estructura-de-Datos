# Arboles-Binarios
class Nodo {
    int valor; // Valor del nodo
    Nodo izquierdo; // Referencia al hijo izquierdo
    Nodo derecho; // Referencia al hijo derecho

    public Nodo(int valor) {
        this.valor = valor; // Inicializa el valor del nodo
        this.izquierdo = null; // Inicializa el hijo izquierdo como nulo
        this.derecho = null; // Inicializa el hijo derecho como nulo
    }
}

class ArbolBinario {
    Nodo raiz; // Nodo raíz del árbol

    public ArbolBinario() {
        this.raiz = null; // Inicializa el árbol vacío
    }

    // Método público para insertar un nuevo valor
    public void insertar(int valor) {
        if (raiz == null) {
            raiz = new Nodo(valor); // Si el árbol está vacío, el nuevo nodo es la raíz
        } else {
            insertarRecursivo(raiz, valor); // Llama al método recursivo para insertar
        }
    }

    // Método privado que maneja la inserción recursiva
    private void insertarRecursivo(Nodo nodo, int valor) {
        if (valor < nodo.valor) { // Si el valor es menor que el nodo actual
            if (nodo.izquierdo == null) {
                nodo.izquierdo = new Nodo(valor); // Inserta a la izquierda si está vacío
            } else {
                insertarRecursivo(nodo.izquierdo, valor); // Recurre hacia la izquierda
            }
        } else { // Si el valor es mayor o igual
            if (nodo.derecho == null) {
                nodo.derecho = new Nodo(valor); // Inserta a la derecha si está vacío
            } else {
                insertarRecursivo(nodo.derecho, valor); // Recurre hacia la derecha
            }
        }
    }

    // Método que realiza un recorrido en orden del árbol
    public void inorden(Nodo nodo) {
        if (nodo != null) {
            inorden(nodo.izquierdo); // Recorre el subárbol izquierdo
            System.out.print(nodo.valor + " "); // Imprime el valor del nodo
            inorden(nodo.derecho); // Recorre el subárbol derecho
        }
    }

    // Método main para probar el árbol
    public static void main(String[] args) {
        ArbolBinario arbol = new ArbolBinario(); // Crea una instancia del árbol
        arbol.insertar(5); // Inserta el valor 5
        arbol.insertar(3); // Inserta el valor 3
        arbol.insertar(7); // Inserta el valor 7
        
        System.out.println("Recorrido en orden:");
        arbol.inorden(arbol.raiz); // Realiza el recorrido en orden e imprime: 3 5 7
    }
}
