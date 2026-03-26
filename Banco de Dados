CREATE DATABASE MonitoramentoIndustrial;
GO

USE MonitoramentoIndustrial;

GO

CREATE TABLE maquinas (
    id_maquina INT AUTO_INCREMENT PRIMARY KEY,
    nome_maquina VARCHAR(100),
    setor VARCHAR(100)
);

CREATE TABLE sensores (
    id_sensor INT AUTO_INCREMENT PRIMARY KEY,
    tipo_sensor VARCHAR(50),
    id_maquina INT,
    FOREIGN KEY (id_maquina) REFERENCES maquinas(id_maquina)
);

CREATE TABLE operadores (
    id_operador INT AUTO_INCREMENT PRIMARY KEY,
    nome_operador VARCHAR(100),
    turno_operador VARCHAR(50)
);

CREATE TABLE leituras (
    id_leitura INT AUTO_INCREMENT PRIMARY KEY,
    valor DECIMAL(5,2),
    data_hora DATETIME,
    id_sensor INT,
    FOREIGN KEY (id_sensor) REFERENCES sensores(id_sensor)
);

CREATE TABLE alertas (
    id_alerta INT AUTO_INCREMENT PRIMARY KEY,
    classificacao_alerta VARCHAR(20),
    id_leitura INT,
    FOREIGN KEY (id_leitura) REFERENCES leituras(id_leitura)
);

CREATE TABLE manutencoes (
    id_manutencao INT AUTO_INCREMENT PRIMARY KEY,
    descricao TEXT,
    data DATE,
    id_maquina INT,
    id_operador INT,
    FOREIGN KEY (id_maquina) REFERENCES maquinas(id_maquina),
    FOREIGN KEY (id_operador) REFERENCES operadores(id_operador)
);
