
# Estrutura do Projeto MVC - QR Code

## Model (Aluno.cs)
```csharp


using System.ComponentModel.DataAnnotations;
using System.ComponentModel.DataAnnotations.Schema;

namespace RecreioFerias.Models
{
    [Table("Aluno")]
    public class Aluno
    {
        [Key()]
        public int AlunoId { get; set; }

        [Display(Name = "Nome do Aluno:")]
        [Required(ErrorMessage = "Campo nome deve ser preenchido.")]
        [MaxLength(100, ErrorMessage = "Campo nome deve ter no maxímo de 255 caracteres.")]
        [MinLength(3, ErrorMessage = "Campo nome deve ter no mínimo de 3 caracteres.")]
        public string Nome { get; set; } = string.Empty;

        [Display(Name = "Nome Social:")]
        [MaxLength(100, ErrorMessage = "Campo nome deve ter no maxímo de 255 caracteres.")]
        [MinLength(3, ErrorMessage = "Campo nome deve ter no mínimo de 3 caracteres.")]
        public string? NomeSocial { get; set; }

        [Display(Name = "RG:")]
        [MaxLength(12, ErrorMessage = "Campo deve ter no maxímo de 12 caracteres.")]
        [MinLength(9, ErrorMessage = "Campo deve ter no mínimo de 9 caracteres.")]
        public string? RG { get; set; }

        [Display(Name = "Data de Expedição RG:")]
        [DisplayFormat(DataFormatString = "{0:dd/MM/yyyy}", ApplyFormatInEditMode = true)]
        [DataType(DataType.Date)]
        public DateOnly? DataExpedicaoRG { get; set; }

        [Display(Name = "CPF:")]
        [MaxLength(14, ErrorMessage = "Campo deve ter no maxímo de 14 caracteres.")]
        [MinLength(14, ErrorMessage = "Campo deve ter no mínimo de 14 caracteres.")]
        public string? CPF { get; set; }

        [Display(Name = "Certidão de Nascimento:")]
        [MaxLength(40, ErrorMessage = "Campo deve ter no maxímo de 40 caracteres.")]
        [MinLength(32, ErrorMessage = "Campo deve ter no mínimo de 32 caracteres.")]
        public string? CertidaoNascimento { get; set; } = string.Empty;

       
        [Display(Name = "Data de Nascimento:")]
        [DisplayFormat(DataFormatString = "{0:dd/MM/yyyy}", ApplyFormatInEditMode = true)]
        [DataType(DataType.Date)]   
        public DateOnly DataNascimento { get; set; }

        [Display(Name = "Sexo:")]
        [Required(ErrorMessage = "Selecione o Sexo.")]
        [MaxLength(20, ErrorMessage = "Campo Genero deve ter no maxímo de 20 caracteres.")]
        public string? Sexo { get; set; }


        [Display(Name = "Responsavel 1:")]
        [Required(ErrorMessage = "Campo nome deve ser preenchido.")]
        public string NomeResponsavel1 { get; set; } = string.Empty;

        [Display(Name = "Social :")]
        public string? NomeResponsavelSocial1 { get; set; }

        [Display(Name = "Telefone Responsavel 1:")]
        [MaxLength(15, ErrorMessage = "Campo Telefone Celular deve ter no maxímo de 14 caracteres.")]
        [MinLength(14, ErrorMessage = "Campo Telefone Celular deve ter no mínimo de 12 caracteres.")]
        [RegularExpression(@"\(\d{2}\) \d{5}-\d{4}", ErrorMessage = "Formato de telefone inválido.")]
        public string TelefoneResponsavel1 { get; set; } = string.Empty;


        [Display(Name = "Outro:")]
        [MaxLength(15, ErrorMessage = "Campo Telefone Celular deve ter no maxímo de 14 caracteres.")]
        [MinLength(14, ErrorMessage = "Campo Telefone Celular deve ter no mínimo de 12 caracteres.")]
        [RegularExpression(@"\(\d{2}\) \d{5}-\d{4}", ErrorMessage = "Formato de telefone inválido.")]
        public string? TelefoneResponsavel1Outro { get; set; }

        [Display(Name = "RG / CPF:")]
        [MaxLength(14, ErrorMessage = "Campo deve ter no maxímo de 14 caracteres.")]
        public string? DocResponsavel1 { get; set; }

        [Display(Name = "Responsavel 2:")]
        public string? NomeResponsavel2 { get; set; }

        [Display(Name = "Telefone Responsavel 2:")]
        [MaxLength(15, ErrorMessage = "Campo Telefone Celular deve ter no maxímo de 14 caracteres.")]
        [MinLength(14, ErrorMessage = "Campo Telefone Celular deve ter no mínimo de 12 caracteres.")]
        [RegularExpression(@"\(\d{2}\) \d{5}-\d{4}", ErrorMessage = "Formato de telefone inválido.")]
        public string? TelefoneResponsavel2 { get; set; }


        [Display(Name = "RG / CPF:")]
        [MaxLength(14, ErrorMessage = "Campo deve ter no maxímo de 14 caracteres.")]
        public string? DocResponsavel2 { get; set; }


        [Display(Name = "Responsavel 3:")]
        public string? NomeResponsavel3 { get; set; }

        [Display(Name = "Telefone Responsavel 3:")]
        [MaxLength(15, ErrorMessage = "Campo Telefone Celular deve ter no maxímo de 14 caracteres.")]
        [MinLength(14, ErrorMessage = "Campo Telefone Celular deve ter no mínimo de 12 caracteres.")]
        [RegularExpression(@"\(\d{2}\) \d{5}-\d{4}", ErrorMessage = "Formato de telefone inválido.")]
        public string? TelefoneResponsavel3 { get; set; }


        [Display(Name = "RG / CPF:")]
        [MaxLength(14, ErrorMessage = "Campo deve ter no maxímo de 14 caracteres.")]
        public string? DocResponsavel3 { get; set; }


        [Display(Name = "Responsavel 4:")]
        public string? NomeResponsavel4 { get; set; }

        [Display(Name = "Telefone Responsavel 4:")]
        [MaxLength(15, ErrorMessage = "Campo Telefone Celular deve ter no maxímo de 14 caracteres.")]
        [MinLength(14, ErrorMessage = "Campo Telefone Celular deve ter no mínimo de 12 caracteres.")]
        [RegularExpression(@"\(\d{2}\) \d{5}-\d{4}", ErrorMessage = "Formato de telefone inválido.")]
        public string? TelefoneResponsavel4 { get; set; }


        [Display(Name = "RG / CPF:")]
        [MaxLength(14, ErrorMessage = "Campo deve ter no maxímo de 14 caracteres.")]
        public string? DocResponsavel4 { get; set; }



        [Display(Name = "CEP:")]
        [MaxLength(8, ErrorMessage = "Campo CEP deve ter no máximo 8 caracteres.")]
        [Required(ErrorMessage ="Preencha o CEP!")]
        public string CEP { get; set; } = string.Empty;

        [Display(Name = "Endereço:")]
        public string Logradouro { get; set; } = string.Empty;
       
        [Display(Name = "Numero:")] 
        public string Numero { get; set; } = string.Empty;

        [Display(Name = "Complemento:")]
        public string? Complemento { get; set; }

        [Display(Name = "Bairro:")]
        public string Bairro { get; set; } = string.Empty;

        [Display(Name = "Cidade:")]
        public string Cidade { get; set; } = string.Empty;

        [Display(Name = "Estado:")]
        public string Estado { get; set; } = string.Empty;

        [DataType(DataType.EmailAddress)]
        public string? Email { get; set; } 

        [Display(Name = "Escola:")]
        [Required(ErrorMessage = "Preencha o Nome da Escola!")]
        public string Escola { get; set; } = string.Empty;

        [Required(ErrorMessage = "Selecione se o Aluno é da Rede Municipal ou Não Estudante da RME!")]
        public bool RedeMunicipal { get; set; }
        [Required(ErrorMessage ="Selecione a Turma do Aluno!")]
        public string AgrupamentoTurmaAno { get; set; } = string.Empty;

        [Display(Name = "Código EOL:")]
        public int? EOL { get; set; }

   
        [Required(ErrorMessage = "Selecione se o Aluno tem Deficiência")]
        public bool OpcaoDeficiencia { get; set; }

        [Required(ErrorMessage = "Selecione se o Aluno tem Algum Problema de Saúde")]
        public bool OpcaoProblemaSaude { get; set; }


  
        [Required(ErrorMessage = "Selecione se o Aluno tem Alguma Restrição Alimentar.")]
        public bool OpcaoRestricaoAlimentar { get; set; }

        
        [Required(ErrorMessage = "Selecione se o Aluno tem Alguma Restrição a algum Medicamento.")]
        public bool OpcaoRestricaoMedicamento { get; set; }

        [Required(ErrorMessage = "Selecione se o Aluno usa Medicamento Contínuo.")]
        public bool OpcaoMedicamento { get; set; }

        [Required(ErrorMessage = "Selecione se o Aluno Possui Convênio Médico")]
        public bool OpcaoConvenioMedico { get; set; }

        public string? Deficiencia { get; set; }

        public string? ProblemaSaude { get; set; }


        public string? RestricaoAlimentar { get; set; }


        public string? RestricaoMedicamento { get; set; }


        public string? Medicamento { get; set; }


        public string? ConvenioMedico { get; set; }


        [Required(ErrorMessage = "Selecione se o Aluno pode Usar a Piscina")]
        public bool Piscina { get; set; }

        
        [Required(ErrorMessage = "Selecione se o Aluno pode Voltar Sozinho")]
        public bool VoltaSozinho { get; set; }

        


        public static List<string> ListaSexo =>
                new List<string>
                {
                    "Masculino", "Feminino", "Outro","Prefiro Não Informar"
                };

        public int CalcularIdade(DateOnly dataNascimento)
        {
            DateTime hoje = DateTime.Today;
            TimeOnly horaPadrao = TimeOnly.MinValue; // Define a hora como 00:00:00

            // Conversão para DateTime
            DateTime dataCompleta = dataNascimento.ToDateTime(horaPadrao);


            int idade = hoje.Year - dataCompleta.Year;
            if (dataCompleta > hoje.AddYears(-idade))
            {
                idade--;
            }
            return idade;
        }

        public int IdadeCalculada => DateTime.Now.Year - DataNascimento.Year -
        (DateTime.Now.DayOfYear < DataNascimento.DayOfYear ? 1 : 0);




    }
}


# Estrutura do Projeto MVC - QR Code

## Controller (Aluno.cs)
```csharp

using Microsoft.AspNetCore.Mvc;
using Microsoft.AspNetCore.Mvc.Rendering;
using Microsoft.EntityFrameworkCore;
using RecreioFerias.Data;
using RecreioFerias.Models;
using X.PagedList.Extensions;
using static RecreioFerias.Controllers.HomeController;

namespace RecreioFerias.Controllers
{
    [ServiceFilter(typeof(RecreioFerias.Filters.AutenticacaoFilter))]
    public class AlunosController : Controller
    {
        private readonly AppDbContext _context;

        public AlunosController(AppDbContext context)
        {
            _context = context;
        }

        // GET: Alunos
        public IActionResult Index(string pesquisa, string filtro, int? page)
        {

            if (pesquisa != null)
            {
                page = 1;
            }
            else
            {
                pesquisa = filtro;
            }


            ViewBag.filtro = pesquisa;
            var consulta = from s in _context.Aluno select s;

            var alunosMatriculados = _context.Matricula.Select(m => m.AlunoId).ToList();
            ViewBag.AlunosMatriculados = alunosMatriculados;

            if (!string.IsNullOrWhiteSpace(pesquisa))
            {
                int id = 0;
                int.TryParse(pesquisa, out id);
                consulta = consulta.Where(t => t.AlunoId == id || t.Nome.Contains(pesquisa));
                

            }

            consulta = consulta.OrderByDescending(s => s.AlunoId);
            int pageSize = 4;
            int pageNumber = (page ?? 1);


            return View(consulta.ToPagedList(pageNumber, pageSize));
        }

     //public async Task<IActionResult> VerificaAluno(string Nome, DateOnly DataNascimento)
     //   {
     //       // Verificar se o Aluno já está cadastrado
     //       var alunoExistente = await _context.Aluno
     //           .FirstOrDefaultAsync(a => a.Nome == Nome && a.DataNascimento == DataNascimento);

     //       if (alunoExistente != null)
     //       {
     //           ModelState.AddModelError("", "O aluno já está cadastrado.");
     //           return RedirectToAction("Create");
     //       }
     //       return RedirectToAction("Create");

     //   }

        // GET: Alunos/Create
        public IActionResult Create()
        {
            ViewBag.List = Aluno.ListaSexo;
            return View();
        }

        // POST: Alunos/Create

        [HttpPost]
        [ValidateAntiForgeryToken]
        public async Task<IActionResult> Create([Bind("AlunoId,Nome,NomeSocial,RG,DataExpedicaoRG,CPF,CertidaoNascimento,DataNascimento,Sexo,NomeResponsavel1,NomeResponsavelSocial1,TelefoneResponsavel1,TelefoneResponsavel1Outro,DocResponsavel1,NomeResponsavel2,TelefoneResponsavel2,DocResponsavel2,NomeResponsavel3,TelefoneResponsavel3,DocResponsavel3,NomeResponsavel4,TelefoneResponsavel4,DocResponsavel4,CEP,Logradouro,Numero,Complemento,Bairro,Cidade,Estado,Email,Escola,RedeMunicipal,AgrupamentoTurmaAno,EOL,OpcaoDeficiencia,OpcaoProblemaSaude,OpcaoRestricaoAlimentar,OpcaoRestricaoMedicamento,OpcaoMedicamento,OpcaoConvenioMedico,Deficiencia,ProblemaSaude,RestricaoAlimentar,RestricaoMedicamento,Medicamento,ConvenioMedico,Piscina,VoltaSozinho")] Aluno aluno)
        {
            ViewBag.List = Aluno.ListaSexo;
            // Transformar o nome para maiúsculo
            aluno.Nome = aluno.Nome.ToUpper();

            if (GetAlunoCadastrado(aluno.Nome, aluno.DataNascimento))
            {
                if (ModelState.IsValid)
                {


                    _context.Add(aluno);
                    await _context.SaveChangesAsync();
                    return RedirectToAction(nameof(Index));
                }
            }
            else
            {
                ModelState.AddModelError("", "O aluno já está cadastrado.");
            }
            return View(aluno);
        }

        // GET: Alunos/Edit/5
        public async Task<IActionResult> Edit(int? id)
        {
            ViewBag.List = Aluno.ListaSexo;
            if (id == null)
            {
                return NotFound();
            }

            var aluno = await _context.Aluno.FindAsync(id);
        
           

            if (aluno == null)
            {
                return NotFound();
            }
            return View(aluno);
        }

        // POST: Alunos/Edit/5
        // To protect from overposting attacks, enable the specific properties you want to bind to.
        // For more details, see http://go.microsoft.com/fwlink/?LinkId=317598.
        [HttpPost]
        [ValidateAntiForgeryToken]
        public async Task<IActionResult> Edit(int id, [Bind("AlunoId,Nome,NomeSocial,RG,DataExpedicaoRG,CPF,CertidaoNascimento,DataNascimento,Sexo,NomeResponsavel1,NomeResponsavelSocial1,TelefoneResponsavel1,TelefoneResponsavel1Outro,DocResponsavel1,NomeResponsavel2,TelefoneResponsavel2,DocResponsavel2,NomeResponsavel3,TelefoneResponsavel3,DocResponsavel3,NomeResponsavel4,TelefoneResponsavel4,DocResponsavel4,CEP,Logradouro,Numero,Complemento,Bairro,Cidade,Estado,Email,Escola,RedeMunicipal,AgrupamentoTurmaAno,EOL,OpcaoDeficiencia,OpcaoProblemaSaude,OpcaoRestricaoAlimentar,OpcaoRestricaoMedicamento,OpcaoMedicamento,OpcaoConvenioMedico,Deficiencia,ProblemaSaude,RestricaoAlimentar,RestricaoMedicamento,Medicamento,ConvenioMedico,Piscina,VoltaSozinho")] Aluno aluno)
        {
            ViewBag.List = Aluno.ListaSexo;
            if (id != aluno.AlunoId)
            {
                return NotFound();
            }
            // Transformar o nome para maiúsculo
            aluno.Nome = aluno.Nome.ToUpper();

            //if (GetAlunoCadastrado(aluno.Nome, aluno.DataNascimento))
            //{
            //    ModelState.AddModelError("", "O aluno já está cadastrado.");
            //}
            if (ModelState.IsValid)
            {
                try
                {
                    var trackedAluno = _context.Aluno.Local.FirstOrDefault(a => a.AlunoId == aluno.AlunoId);
                    if (trackedAluno != null)
                    {
                        _context.Entry(trackedAluno).CurrentValues.SetValues(aluno);
                    }
                    else
                    {
                        _context.Update(aluno);
                    }
                    await _context.SaveChangesAsync();
                }
                catch (DbUpdateConcurrencyException)
                {
                    if (!AlunoExists(aluno.AlunoId))
                    {
                        return NotFound();
                    }
                    else
                    {
                        throw;
                    }
                }
                return RedirectToAction(nameof(Index));
            }
            return View(aluno);
        }

        // GET: Alunos/Delete/5
        public async Task<IActionResult> Delete(int? id)
        {
            if (id == null)
            {
                return NotFound();
            }

            var aluno = await _context.Aluno
                .FirstOrDefaultAsync(m => m.AlunoId == id);
            if (aluno == null)
            {
                return NotFound();
            }

            return View(aluno);
        }

        // POST: Alunos/Delete/5
        [HttpPost, ActionName("Delete")]
        [ValidateAntiForgeryToken]
        public async Task<IActionResult> DeleteConfirmed(int id)
        {
            var aluno = await _context.Aluno.FindAsync(id);
            if (aluno != null)
            {
                _context.Aluno.Remove(aluno);
            }

            await _context.SaveChangesAsync();
            return RedirectToAction(nameof(Index));
        }

        private bool AlunoExists(int id)
        {
            return _context.Aluno.Any(e => e.AlunoId == id);
        }

        public bool GetAlunoCadastrado(string Nome, DateOnly DataNascimento)
        {
            var alunoCadastrado = _context.Aluno.FirstOrDefault(t => t.Nome.Contains(Nome) && t.DataNascimento == DataNascimento);
            if (alunoCadastrado != null)
            {
                return false;
            }



            return true;
        }
    }
}

# Estrutura do Projeto MVC - QR Code

## View (Aluno/index.cshtml)
```csharp

@using X.PagedList.Mvc.Core
@model X.PagedList.IPagedList<RecreioFerias.Models.Aluno>

@{
    ViewData["Title"] = "Cadastro de Alunos";
    Layout = "~/Views/Shared/_Layout.cshtml";
    var alunosMatriculados = ViewBag.AlunosMatriculados as List<int>;
}

<h2 class="titulo-aluno">Cadastro de Alunos</h2>

<br />
<div class="container">
    <div class="row">
        <div class="col-lg-6">
            <a asp-action="Create" class="btn btn-success"
            aria-label="Botão adicionar novo aluno" 
            
            >
                <i class="bi bi-file-earmark-plus" aria-hidden="true" style="font-size: 1.5rem;"></i>&#32 Alunos
            </a>
        </div>
        <div class="col-lg-6 fs-personalizado fonte-login">
            <form asp-action="Index" asp-controller="Alunos" method="post">
             <label for="pesquisa" class="form-label">Pesquisar:</label>
             <input name="pesquisa" id="pesquisa" value="@ViewBag.filtro" />

<button class="btn btn-outline-secondary small" style="color:darkblue" type="submit"
    aria-label="Pesquisar alunos">
    <i class="bi bi-search" aria-hidden="true"></i>  
</button>

<button class="btn btn-outline-info small" style="color:blueviolet" onclick="limparInput()"
    aria-label="Limpar Campo">
    <i class="bi bi-eraser" aria-hidden="true"></i>
</button>
            </form>
        </div>
    </div>
    <div><br /></div>
</div>
<table class=" table table-condensed table-hover table-striped fs-tabela fonte-login">
    <thead>
        <tr>
            <th>
                Nome
            </th>
            <th>
                Idade
            </th>
            <th>
                Responsavel
            </th>

            <th>
                Telefone
            </th>
            <th>
                Telefone 2
            </th>
            <th>
                Uso da Piscina
            </th>
            <th>
                Restrições
            </th>
            <th>
                Volta Sozinho
            </th>
            
            
        </tr>
    </thead>
    <tbody>
        @foreach (var item in Model)
        {
            <tr>
                <td>
                    @Html.DisplayFor(modelItem => item.Nome)
                </td>
                <td>

                    <span>@item.CalcularIdade(item.DataNascimento)</span>
                    
                </td>

                <td>
                    @Html.DisplayFor(modelItem => item.NomeResponsavel1)
                </td>

                <td>
                    @Html.DisplayFor(modelItem => item.TelefoneResponsavel1)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.TelefoneResponsavel1Outro)
                </td>
                <td>
                    @if (item.Piscina)
                    {
                        <span>Sim</span>
                    }
                    else
                    {
                        <span>Não</span>
                    }

                </td>

                <td>
                    @Html.DisplayFor(modelItem => item.ProblemaSaude)
                    @Html.DisplayFor(modelItem => item.RestricaoAlimentar)
                    @Html.DisplayFor(modelItem => item.RestricaoMedicamento)
                    @Html.DisplayFor(modelItem => item.Medicamento)
                </td>

                <td>
                    @if (item.VoltaSozinho)
                    {
                    <span>Sim</span>
                    }
                    else
                    {
                        <span>Não</span>
                    }

                </td>
                <td>
                   
                    <a asp-action="Edit" asp-route-id="@item.AlunoId" class="btn btn-warning aria-label="Editar item"
                    aria-label="Editar Aluno">
                        <i class="bi bi-pencil" style="vertical-align: middle; border:1px; color:white;"></i>
                    </a>
                    <a asp-action="Delete" asp-route-id="@item.AlunoId" class="btn btn-danger" aria-label="Deletar aluno">
                        <i class="bi bi-trash" style="vertical-align: middle;"></i>
                    </a>
                   @*  <a asp-controller="Matriculas" asp-action="Create" asp-route-id="@item.AlunoId" class="btn btn-primary">
                        <i class="bi bi-emoji-laughing-fill" style="vertical-align: middle;"></i> Matricular
                    </a> *@
                    <a class="btn btn-primary @(alunosMatriculados.Contains(item.AlunoId) ? "disabled" : "")"
                   @(alunosMatriculados.Contains(item.AlunoId) ? "tabindex='-1' aria-disabled='true'" : "")
                   href="@(alunosMatriculados.Contains(item.AlunoId) ? "#" : Url.Action("Create", "Matriculas", new { id = item.AlunoId }))">
    
                   <i class="bi bi-emoji-laughing-fill" style="vertical-align: middle;" aria-hidden="true"></i> Matricular
</a>

                </td>
            </tr>
        }
    </tbody>
</table>
<div>
    <div style="float: right">
        Página @(Model.PageCount < Model.PageNumber ? 0 : Model.PageNumber) de @Model.PageCount
    </div>

    <div class="justify-content-center">
        @Html.PagedListPager(
                 Model,
                 page => Url.Action("Index", new { page, filtro = ViewBag.filtro }),
                 new PagedListRenderOptions
        {

            LiElementClasses = new[] { "page-item" },
            UlElementClasses = new[] { "pagination justify-content-center" }
        }
                 )
    </div>
</div>