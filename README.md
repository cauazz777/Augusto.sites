import { Button } from "@/components/ui/button";
import { Card } from "@/components/ui/card";
import { Dialog, DialogContent, DialogHeader, DialogTitle, DialogTrigger } from "@/components/ui/dialog";
import { Phone, Code, Smartphone, Globe, MessageCircle, Instagram, ExternalLink } from "lucide-react";

const Index = () => {
  const phoneNumber = "5517992239910"; // WhatsApp format
  const message = "Olá Augusto-Desenvolvedor-sites Quero Desenvolver um Site Com Você!";
  
  const projects = [
    {
      title: "Blog Homepage",
      description: "Layout moderno para página inicial de blog",
      url: "https://flowbite.com/marketing-ui/preview/?page=blog/homepage/"
    },
    {
      title: "Artigo de Blog", 
      description: "Template elegante para artigos e posts",
      url: "https://flowbite.com/marketing-ui/preview/?page=blog/article/"
    },
    {
      title: "Página de Equipe",
      description: "Apresentação profissional da equipe",
      url: "https://flowbite.com/marketing-ui/preview/?page=team/team-2/"
    },
    {
      title: "Landing Page Agência",
      description: "Site completo para agências digitais", 
      url: "https://flowbite.com/marketing-ui/preview/?page=landing/agency/"
    }
  ];
  
  const handleWhatsAppClick = () => {
    const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
    window.open(whatsappUrl, '_blank');
  };

  const handleInstagramClick = () => {
    window.open('https://www.instagram.com/augusto_sites/', '_blank');
  };

  const handlePortfolioClick = () => {
    window.open('https://vicentina-care-hub-85.lovable.app', '_blank');
  };

  const handleServiceClick = (serviceType: string) => {
    const messageWithService = `${message} - ${serviceType}`;
    const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(messageWithService)}`;
    window.open(whatsappUrl, '_blank');
  };

  return (
    <div className="min-h-screen bg-background">
      {/* Header */}
      <header className="border-b border-secondary bg-background/95 backdrop-blur-sm sticky top-0 z-50">
        <div className="container mx-auto px-4 py-4">
          <div className="flex items-center justify-between">
            <div className="flex items-center gap-4">
              <div className="h-12 w-12 bg-gradient-to-br from-primary to-primary-glow rounded-lg flex items-center justify-center">
                <Code className="h-6 w-6 text-white" />
              </div>
              <h1 className="text-2xl md:text-3xl font-bold text-white tracking-tight animate-pulse-slow">
                Augusto-Desenvolvedor-sites
              </h1>
            </div>
            <nav className="flex items-center gap-6">
              <a href="#" className="text-white hover:text-primary transition-colors font-medium">
                Início
              </a>
              <a href="#projeto" className="text-white hover:text-primary transition-colors font-medium">
                Projeto
              </a>
              <Button 
                onClick={handleWhatsAppClick}
                variant="outline"
                size="sm"
                className="border-primary text-primary hover:bg-primary hover:text-primary-foreground"
              >
                <MessageCircle className="mr-2 h-4 w-4" />
                Contato
              </Button>
            </nav>
          </div>
        </div>
      </header>

      {/* Services Overview Section */}
      <section id="projeto" className="py-16 bg-gradient-to-br from-secondary via-background to-secondary">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl md:text-4xl font-bold text-center mb-12 text-white">
            Qual Seria O Assunto Sobre Seu Site
          </h2>
          
          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-6 max-w-7xl mx-auto">
            <Card 
              className="p-6 bg-card/50 backdrop-blur-sm border-secondary hover:border-primary transition-all duration-300 cursor-pointer"
              onClick={() => handleServiceClick("Para um público mais profissional")}
            >
              <div className="text-2xl mb-4">💼</div>
              <h3 className="text-lg font-bold mb-3 text-primary">Para um público mais profissional</h3>
              <h4 className="text-base font-semibold mb-2 text-white">Seu negócio merece um site à altura.</h4>
              <p className="text-muted-foreground text-sm">
                Chega de perder oportunidades por não estar online! Eu crio sites profissionais, rápidos e que passam confiança para seus clientes. Vamos construir a presença digital que sua empresa precisa.
              </p>
            </Card>

            <Card 
              className="p-6 bg-card/50 backdrop-blur-sm border-secondary hover:border-primary transition-all duration-300 cursor-pointer"
              onClick={() => handleServiceClick("Para lojas e pequenos empreendedores")}
            >
              <div className="text-2xl mb-4">🛍️</div>
              <h3 className="text-lg font-bold mb-3 text-primary">Para lojas e pequenos empreendedores</h3>
              <h4 className="text-base font-semibold mb-2 text-white">Venda mais com um site que trabalha por você!</h4>
              <p className="text-muted-foreground text-sm">
                Tenha uma loja virtual ou página de vendas que funciona 24 horas por dia, do seu jeito. Sites bonitos, prontos pra vender e fáceis de usar. Bora fazer o seu?
              </p>
            </Card>

            <Card 
              className="p-6 bg-card/50 backdrop-blur-sm border-secondary hover:border-primary transition-all duration-300 cursor-pointer"
              onClick={() => handleServiceClick("Para criativos, artistas ou portfólios")}
            >
              <div className="text-2xl mb-4">🎨</div>
              <h3 className="text-lg font-bold mb-3 text-primary">Para criativos, artistas ou portfólios</h3>
              <h4 className="text-base font-semibold mb-2 text-white">Mostre seu talento com um site único.</h4>
              <p className="text-muted-foreground text-sm">
                Seja artista, designer, fotógrafo ou criador: seu trabalho merece destaque. Eu te ajudo a criar um portfólio online que representa quem você é — com estilo, identidade e profissionalismo.
              </p>
            </Card>

            <Card 
              className="p-6 bg-card/50 backdrop-blur-sm border-secondary hover:border-primary transition-all duration-300 cursor-pointer"
              onClick={() => handleServiceClick("Mais descontraído e direto")}
            >
              <div className="text-2xl mb-4">😎</div>
              <h3 className="text-lg font-bold mb-3 text-primary">Mais descontraído e direto</h3>
              <h4 className="text-base font-semibold mb-2 text-white">Quer um site bonito, rápido e do seu jeito?</h4>
              <p className="text-muted-foreground text-sm">
                Eu crio sites que chamam atenção, funcionam bem no celular e ajudam você a crescer online. Me chama e bora tirar seu site do papel!
              </p>
            </Card>
          </div>
        </div>
      </section>

      {/* Hero Section */}
      <section className="relative py-20 overflow-hidden">
        <div className="absolute inset-0 bg-gradient-to-br from-background via-secondary to-background"></div>
        <div className="absolute inset-0 bg-grid-pattern opacity-10"></div>
        <div className="container mx-auto px-4 text-center relative z-10">
          <h2 className="text-4xl md:text-6xl font-bold mb-6 text-white tracking-tight">
            Crie Seu Site com Ótima Qualidade
          </h2>
          <p className="text-xl md:text-2xl text-muted-foreground mb-12 max-w-3xl mx-auto leading-relaxed">
            Desenvolvimento de sites modernos, responsivos e otimizados para seu negócio crescer na internet
          </p>
          <div className="flex flex-col sm:flex-row gap-4 justify-center items-center">
            <Button 
              onClick={handleWhatsAppClick}
              size="lg" 
              className="glow-effect text-lg px-10 py-5 hover:scale-105 transition-all duration-300 bg-gradient-to-r from-primary to-primary-glow"
            >
              <MessageCircle className="mr-2 h-5 w-5" />
              Solicitar Orçamento
            </Button>
            <Button 
              onClick={handlePortfolioClick}
              variant="outline" 
              size="lg"
              className="border-primary/50 text-white hover:bg-primary/10 hover:border-primary transition-all duration-300 backdrop-blur-sm"
            >
              <Globe className="mr-2 h-5 w-5" />
              Ver Portfolio
            </Button>
          </div>
        </div>
      </section>

      {/* Services Section */}
      <section className="py-20">
        <div className="container mx-auto px-4">
          <h3 className="text-3xl md:text-4xl font-bold text-center mb-16">
            Meus <span className="text-primary">Serviços</span>
          </h3>
          
           <div className="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
             <Card 
               className="p-8 bg-card/50 backdrop-blur-sm border-secondary hover:border-primary transition-all duration-300 cursor-pointer group relative overflow-hidden"
               onClick={handlePortfolioClick}
             >
               <div className="absolute inset-0 bg-gradient-to-br from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
               <div className="relative z-10">
                 <div className="text-primary mb-6 flex items-center justify-between">
                   <Globe className="h-16 w-16" />
                   <ExternalLink className="h-6 w-6 opacity-0 group-hover:opacity-100 transition-all duration-300 transform group-hover:scale-110" />
                 </div>
                  <h4 className="text-2xl font-bold mb-4">Sites Criado Por Mim Que Estão Em Usos</h4>
                  <p className="text-muted-foreground text-lg">
                    Sites profissionais para empresas, apresentando seus serviços de forma elegante e moderna. Clique para ver meus trabalhos.
                  </p>
               </div>
             </Card>

              <Dialog>
                <DialogTrigger asChild>
                  <Card 
                    className="p-8 bg-card/50 backdrop-blur-sm border-secondary hover:border-primary transition-all duration-300 cursor-pointer group relative overflow-hidden"
                  >
                    <div className="absolute inset-0 bg-gradient-to-br from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                    <div className="relative z-10">
                      <div className="text-primary mb-6 flex items-center justify-between">
                        <Code className="h-16 w-16" />
                        <ExternalLink className="h-6 w-6 opacity-0 group-hover:opacity-100 transition-all duration-300 transform group-hover:scale-110" />
                      </div>
                      <h4 className="text-2xl font-bold mb-4">Meus Projetos De Sites</h4>
                      <p className="text-muted-foreground text-lg">
                        Aplicações web personalizadas com as tecnologias mais modernas do mercado. Clique para ver meus trabalhos.
                      </p>
                    </div>
                  </Card>
                </DialogTrigger>
                <DialogContent className="max-w-4xl max-h-[80vh] overflow-y-auto">
                  <DialogHeader>
                    <DialogTitle className="text-2xl font-bold mb-6">Meus Projetos De Sites</DialogTitle>
                  </DialogHeader>
                  <div className="grid md:grid-cols-2 gap-6">
                    {projects.map((project, index) => (
                      <Card key={index} className="p-6 bg-card border-secondary hover:border-primary transition-colors cursor-pointer group"
                            onClick={() => window.open(project.url, '_blank')}>
                        <div className="flex items-center justify-between mb-4">
                          <h5 className="text-lg font-semibold">{project.title}</h5>
                          <ExternalLink className="h-5 w-5 text-primary opacity-0 group-hover:opacity-100 transition-opacity" />
                        </div>
                        <p className="text-muted-foreground text-sm">{project.description}</p>
                      </Card>
                    ))}
                  </div>
                </DialogContent>
              </Dialog>
           </div>
        </div>
      </section>

      {/* About Section */}
      <section className="py-20 bg-gradient-to-br from-background via-secondary to-background">
        <div className="container mx-auto px-4 text-center">
          <div className="max-w-4xl mx-auto">
            <h3 className="text-3xl md:text-4xl font-bold mb-8 text-white">
              Transforme sua ideia em um <span className="text-primary">site profissional!</span>
            </h3>
            <p className="text-xl text-muted-foreground leading-relaxed mb-8">
              Você tem um negócio, projeto ou marca pessoal e quer marcar presença online? Eu posso te ajudar a criar um site moderno, responsivo e feito sob medida pra você. Entre em contato e vamos tirar sua ideia do papel!
            </p>
            <div className="flex flex-col sm:flex-row gap-4 justify-center items-center">
              <Button 
                onClick={handleWhatsAppClick}
                size="lg" 
                className="glow-effect text-lg px-10 py-5 hover:scale-105 transition-all duration-300 bg-gradient-to-r from-primary to-primary-glow"
              >
                <Phone className="mr-2 h-5 w-5" />
                (17) 99223-0910
              </Button>
              <Button 
                onClick={handleWhatsAppClick}
                variant="outline" 
                size="lg"
                className="border-primary/50 text-white hover:bg-primary/10 hover:border-primary transition-all duration-300 backdrop-blur-sm"
              >
                <MessageCircle className="mr-2 h-5 w-5" />
                Fale Comigo Agora
              </Button>
            </div>
          </div>
        </div>
      </section>


      {/* Footer */}
      <footer className="py-8 border-t border-secondary text-center">
        <div className="container mx-auto px-4">
          <div className="flex flex-col items-center gap-4">
            <Button
              onClick={handleInstagramClick}
              variant="outline"
              size="sm"
              className="border-primary text-primary hover:bg-primary hover:text-primary-foreground"
            >
              <Instagram className="mr-2 h-4 w-4" />
              @augusto_sites
            </Button>
            <p className="text-muted-foreground">
              Obrigado Por Escolher Augusto-Desenvolvedor-sites
            </p>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default Index;
