package org.example;

import java.util.Date;

public class Main {
    public Main() {
    }
    public static void main(String[] args) {
        Pedido pedido = new Pedido(25, new Date(), 10.5, "Prueba");
        pedido.solicitar();
        pedido.cancelarPedido();
        pedido.calcularTotal();
        pedido.reiniciarEstado();

        Cliente cliente = new Cliente(1, "Joel", "Calle 143", "123456789", "joel@example.com", 30);

        cliente.agregarPedido(new Pedido(25, new Date(), 10.5, "Prueba"));
        cliente.eliminarPedido(new Pedido(25, new Date(), 10.5, "Prueba"));
        cliente.actualizarDatos();
        cliente.verHistorial();
    }
}
