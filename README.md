// import static org.junit.jupiter.api.Assertions.assertEquals;

// import org.junit.jupiter.api.Test;
import java.util.ArrayList;
import java.util.List;

  public class Main {
  public static void main(String[] args) {

    // Classe do produto
  class Produto {
    private int id;
    private String nome;
    private float preco;
    private int estoque;

  public Produto(int id, String nome, float preco, int estoque) {
      this.id = id;
      this.nome = nome;
      this.preco = preco;
      this.estoque = estoque;
            }

  public void atualizarEstoque(int quantidade) {
                estoque += quantidade;
            }
  public int getId() {
   return id;
            }
  public String getNome() {
   return nome;
            }
  public float getPreco() {
    return preco;
            }
  public int getEstoque() {
    return estoque;
            }
  public void setEstoque(int estoque) {
      this.estoque = estoque;
            }
        }
  // Classe cliente
  class Cliente {
       private int id;
       private String nome;
       private int CPF;

  public Cliente(int id, String nome, int CPF) {
        this.id = id;
        this.nome = nome;
        this.CPF = CPF;
            }
  public int getId() {
         return id;
            }
  public String getNome() {
                return nome;
            }
  public int getCPF() {
                return CPF;
            }
        }

// Classe carrinho
   class Carrinho {
       private int id;
       private Cliente cliente;
       private List<Produto> produtos;

   public Carrinho(int id, Cliente cliente) {
        this.id = id;
        this.cliente = cliente;
        this.produtos = new ArrayList<>();
            }

    public void adicionarProduto(Produto produto) {
           produtos.add(produto);
            }

    public float calcularTotal() {
           float total = 0;
           for (Produto produto : produtos) {
           total += produto.getPreco();
                }
            return total;
            }
    public int getId() {
             return id;
            }

    public Cliente getCliente() {
              return cliente;
            }
    public List<Produto> getProdutos() {
                return produtos;
            }
        }
    }
  }
    

  // @Test
  // void addition() {
  //     assertEquals(2, 1 + 1);
  // }# store-software
the goal on this class was to build a code for a previus diagram we did in class
