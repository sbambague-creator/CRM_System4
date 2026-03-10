package src.crm.modelo;

import java.time.LocalDateTime;

public class Cliente {
    private int id;
    private String nombreEmpresa;
    private String telefono;
    private String correo;
    private LocalDateTime fechaRegistro;

    public Cliente(int id, String nombreEmpresa, String telefono, String correo, LocalDateTime fechaRegistro) {
        this.id = id;
        this.nombreEmpresa = nombreEmpresa;
        this.telefono = telefono;
        this.correo = correo;
        this.fechaRegistro = fechaRegistro;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getNombreEmpresa() {
        return nombreEmpresa;
    }

    public void setNombreEmpresa(String nombreEmpresa) {
        this.nombreEmpresa = nombreEmpresa;
    }

    public String getTelefono() {
        return telefono;
    }

    public void setTelefono(String telefono) {
        this.telefono = telefono;
    }

    public String getCorreo() {
        return correo;
    }

    public void setCorreo(String correo) {
        this.correo = correo;
    }

    public LocalDateTime getFechaRegistro() {
        return fechaRegistro;
    }

    public void setFechaRegistro(LocalDateTime fechaRegistro) {
        this.fechaRegistro = fechaRegistro;
    }

    public void consultarCliente() {
        System.out.println("=== Información del Cliente ===");
        System.out.println("ID: " + id);
        System.out.println("Empresa: " + nombreEmpresa);
        System.out.println("Teléfono: " + telefono);
        System.out.println("Correo: " + correo);
        System.out.println("Fecha de Registro: " + fechaRegistro);
        System.out.println("===============================");
    }
    
}

