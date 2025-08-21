import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { motion } from "framer-motion";
import { CheckCircle } from "lucide-react";

export default function LandingPage() {
  return (
    <div className="bg-gray-50 min-h-screen text-gray-800">
      {/* Hero Section */}
      <section className="bg-gradient-to-r from-yellow-400 to-orange-500 text-white py-20 px-6 text-center">
        <h1 className="text-4xl font-bold mb-4">
          🌟 Escuta Individual Sistêmica Comportamental Empresarial
        </h1>
        <p className="text-lg max-w-2xl mx-auto">
          Descubra o que está travando sua vida e seu negócio – e receba um
          diagnóstico personalizado para destravar seus resultados.
        </p>
        <Button className="mt-6 text-lg px-6 py-3 rounded-2xl shadow-lg">
          Quero minha Escuta Sistêmica
        </Button>
      </section>

      {/* Dor Section */}
      <section className="py-16 px-6 max-w-5xl mx-auto grid md:grid-cols-2 gap-10">
        <div>
          <h2 className="text-2xl font-bold mb-4">🔥 Você já se sentiu assim?</h2>
          <ul className="space-y-3">
            {[
              "Trabalha demais e mesmo assim parece que não sai do lugar?",
              "Sente medo de crescer e ‘não dar conta’?",
              "Percebe conflitos familiares ou emocionais refletindo no seu negócio?",
              "Já se perguntou por que repete os mesmos padrões, mesmo querendo mudar?",
            ].map((item, i) => (
              <li key={i} className="flex items-start gap-2">
                <CheckCircle className="text-yellow-500 mt-1" size={20} />
                <span>{item}</span>
              </li>
            ))}
          </ul>
        </div>
        <Card className="shadow-xl rounded-2xl">
          <CardContent className="p-6">
            <p className="text-lg">
              👉 Nada disso acontece por acaso. Muitos empresários carregam
              <strong> bloqueios invisíveis</strong> que afetam diretamente a
              gestão, a liderança e os resultados.
            </p>
          </CardContent>
        </Card>
      </section>

      {/* O que é */}
      <section className="bg-white py-16 px-6 text-center">
        <h2 className="text-2xl font-bold mb-6">💡 O que é a Escuta Sistêmica?</h2>
        <p className="max-w-3xl mx-auto text-lg">
          Um processo profundo, rápido e transformador, que conecta vida pessoal
          e empresarial. Você terá clareza sobre:
        </p>
        <div className="grid md:grid-cols-2 gap-6 mt-10 max-w-4xl mx-auto">
          {[
            "Os padrões que se repetem na sua história",
            "O que está bloqueando seus resultados hoje",
            "Como alinhar vida, liderança e negócio",
            "Passos práticos para construir prosperidade com leveza",
          ].map((item, i) => (
            <Card key={i} className="shadow-md rounded-2xl">
              <CardContent className="p-6 flex items-center gap-3">
                <CheckCircle className="text-green-500" />
                <span>{item}</span>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Como funciona */}
      <section className="bg-gray-100 py-16 px-6 text-center">
        <h2 className="text-2xl font-bold mb-6">🚀 Como funciona?</h2>
        <div className="grid md:grid-cols-3 gap-8 max-w-5xl mx-auto">
          {[
            {
              title: "Primeira Sessão – Escuta",
              desc: "Você compartilha sua história e identificamos os pontos-chave que limitam seu crescimento.",
            },
            {
              title: "Segunda Sessão – Devolutiva Oral",
              desc: "Apresentamos o diagnóstico sistêmico e orientações iniciais para começar a destravar resultados.",
            },
            {
              title: "Devolutiva Escrita Personalizada",
              desc: "Em até 10 dias, você recebe um documento exclusivo com recomendações adaptadas ao seu momento.",
            },
          ].map((step, i) => (
            <Card key={i} className="shadow-md rounded-2xl">
              <CardContent className="p-6">
                <h3 className="font-bold mb-2">{step.title}</h3>
                <p>{step.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Investimento */}
      <section className="bg-white py-16 px-6 text-center">
        <h2 className="text-2xl font-bold mb-6">💰 Investimento Promocional</h2>
        <div className="flex flex-col md:flex-row justify-center gap-8 max-w-4xl mx-auto">
          <Card className="shadow-lg rounded-2xl w-full md:w-1/3">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold">Individual</h3>
              <p className="text-3xl font-semibold text-yellow-600 mt-2">R$ 497</p>
            </CardContent>
          </Card>
          <Card className="shadow-lg rounded-2xl w-full md:w-1/3">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold">Dupla de Sócios</h3>
              <p className="text-3xl font-semibold text-yellow-600 mt-2">R$ 897</p>
            </CardContent>
          </Card>
        </div>
        <p className="mt-6 italic">
          *Preço especial de lançamento – vagas limitadas por ser um trabalho individualizado.
        </p>
        <Button className="mt-8 text-lg px-6 py-3 rounded-2xl shadow-lg">
          Quero minha Escuta Sistêmica
        </Button>
      </section>
    </div>
  );
}
