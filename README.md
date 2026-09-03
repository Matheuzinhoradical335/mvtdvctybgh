/Avaliação//

Data: 02/09/2026

Avaliação realizada por - PAULO DAVI DE MELO;

Avaliando projeto de - MATHEUS ALEXANDRE BENÍCIO DE ARAÚJO;

/Avaliação//

Avaliação - Organização bem estruturada, o aluno respeitou a hierarquia das tags de título e utilizou corretamente os elementos semânticos, como header, main, section e footer, no lugar de divs genéricas. O formulário foi feito de forma coerente com o tema proposto, com os diferentes campos de tipos semanticamente corretos, como tel para telefone e number com min/max para a avaliação da loja; o required foi utilizado respeitando o mínimo necessário e os labels foram corretamente associados aos inputs via for/id. Como sugestão de melhoria, vale a pena unificar os três formulários (materiais básicos, ferramentas e dados de entrega) em um único formulário — assim, ao finalizar o pedido, todos os itens selecionados são enviados junto com os dados de entrega, incluindo também o campo de avaliação da loja no mesmo envio.



<!DOCTYPE html> 
<html lang="pt-BR"> 
    <head> 
        <!-- Meta charset essencial para acentuação correta[span_1](start_span)[span_1](end_span) -->
        <meta charset="UTF-8"> 
        <title>CONSTRUBEM - MATERIAIS DE CONSTRUÇÃO</title>   
    </head> 
 
    <body> 
        <header> 
            <h1>CONSTRUBEM - MATERIAIS DE CONSTRUÇÃO</h1> 
            <p>Tudo para a sua obra, do alicerce ao telhado!</p> 
            <h2>Nossa Localização: </h2> 
            <p>Avenida dos Construtores, 456 - Centro, XXXXX - XXX</p> 
        </header> 
 
        <main> 
            <section> 
                <h2>Catálogo de Produtos:</h2> 
                <p>Selecione os itens desejados abaixo.</p> 
                <p><strong>Lembre-se de preencher seus dados de entrega ao fim do pedido!</strong></p> 
            </section> 
 
            <!-- Seção de Materiais Básicos -->
            <section> 
                <h2>Materiais Básicos:</h2> 
                <form> 
                    <input type="checkbox" value="Cimento 50kg" id="MBa" name="MaterialBasico"> 
                    <!-- Associação correta do for com o id do input[span_2](start_span)[span_2](end_span) -->
                    <label for="MBa">Saco de Cimento 50kg <strong>(R$ 35,00)</strong></label><br> 
 
                    <input type="checkbox" value="Tijolo 8 furos" id="MBb" name="MaterialBasico"> 
                    <label for="MBb">Milheiro de Tijolo 8 Furos <strong>(R$ 600,00)</strong></label><br> 

                    <input type="checkbox" value="Areia fina" id="MBc" name="MaterialBasico"> 
                    <label for="MBc">Metro de Areia Fina <strong>(R$ 120,00)</strong></label><br> 
                </form> 
             </section> 

            <!-- Seção de Ferramentas -->
            <section> 
                <h2>Ferramentas:</h2> 
                <form> 
                    <input type="checkbox" value="Martelo" id="FEa" name="Ferramentas"> 
                    <label for="FEa">Martelo com cabo de madeira <strong>(R$ 25,00)</strong></label><br> 
 
                    <input type="checkbox" value="Furadeira" id="FEb" name="Ferramentas"> 
                    <label for="FEb">Furadeira de Impacto 500W <strong>(R$ 150,00)</strong></label><br> 
                </form> 
             </section> 
        </main> 
 
        <footer> 
            <h2>Formulário para a entrega:</h2> 
            <!-- Um único formulário agrupando os dados do cliente[span_3](start_span)[span_3](end_span) -->
            <form> 
                <fieldset> 
                    <legend>Preencha todas as informações</legend> 
                    
                    <label for="Nm">Nome do Responsável pela Obra:</label> 
                    <input type="text" id="Nm" name="Nome" placeholder="Digite seu nome aqui..." required> <br><br>
                    
                    <label for="tlf">Telefone (WhatsApp):</label> 
                    <!-- type="tel" aciona o teclado numérico em celulares[span_4](start_span)[span_4](end_span) -->
                    <input type="tel" id="tlf" name="Telefone" placeholder="(00) 00000-0000" required> <br><br>
     
                    <label for="pagamento">Forma de pagamento (no ato da entrega):</label> 
                    <!-- Tag select para lista suspensa[span_5](start_span)[span_5](end_span) -->
                    <select name="pagamento" id="pagamento" required> 
                        <option value="">Selecione...</option> 
                        <option value="Dinheiro">Dinheiro</option> 
                        <option value="PIX">PIX</option> 
                        <option value="Cartão de crédito">Cartão de crédito</option> 
                        <option value="Cartão de débito">Cartão de débito</option> 
                    </select> <br><br>
     
                    <label for="End">Endereço da Obra:</label> 
                    <input type="text" id="End" name="Endereço" placeholder="Rua, número, bairro..." required> <br><br>
     
                    <label for="PTR">Ponto de referência:</label> 
                    <input type="text" id="PTR" name="Ponto de referência" placeholder="Ex: Próximo ao mercado..."> 
                </fieldset> 
                
                <br><button type="submit">Finalizar Pedido de Materiais</button><br> 
            </form>

            <section>
                <h2>Avalie nosso atendimento!</h2> 
                <label for="ava">Nota para a loja (de 1 a 5 estrelas):</label> <br>
                <!-- Uso de validação nativa min e max no input numérico[span_6](start_span)[span_6](end_span) -->
                <input type="number" id="ava" name="avaliação" min="1" max="5" placeholder="Sua nota..."> 
            </section>
        </footer> 
    </body> 
</html>
