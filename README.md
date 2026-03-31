/* CARD PRINCIPAL */
.card-perfil {
  position: relative;
  width: 90%;
  max-width: 350px;
  margin: 80px auto;
  padding: 80px 20px 30px;
  background: linear-gradient(180deg, #1e1e2f, #2a2a4a);
  border-radius: 20px;
  text-align: center;
  color: white;
}

/* FOTO SOBREPOSTA */
.perfil-container {
  position: absolute;
  top: -60px;
  left: 50%;
  transform: translateX(-50%);
}

.foto-perfil {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #4b0082;
}

/* TEXTO */
.nome {
  margin-top: 10px;
  font-size: 20px;
}

.descricao {
  font-size: 14px;
  margin-bottom: 20px;
  color: #ccc;
}

/* BOTÕES */
.botoes {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.botoes button {
  padding: 10px;
  border-radius: 20px;
  border: none;
  background: #fff;
  color: #333;
  font-weight: bold;
  cursor: pointer;
}

/* RESPONSIVO */
@media (min-width: 600px) {
  .botoes {
    flex-direction: row;
    justify-content: center;
  }
}
import Imagens from "../../Imagens/fotoPerfil.jpeg";
import "./estilo.css";

function Perfil() {
  return (
    <div className="card-perfil">
      
      <div className="perfil-container">
        <img src={Imagens} alt="Minha foto" className="foto-perfil" />
      </div>

      <h2 className="nome">Seu Nome</h2>
      <p className="descricao">Desenvolvedora Front-End em formação</p>

      <div className="botoes">
        <button>Email</button>
        <button>LinkedIn</button>
        <button>GitHub</button>
      </div>

    </div>
  );
}

export default Perfil;
