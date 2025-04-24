/ KzInvest - Plataforma de Investimento em Kwanza
        <h1 className="text-4xl font-bold text-green-700">KzInvest</h1>
function Dashboard() {
  return (
    <div className="max-w-5xl mx-auto">
      <section className="mb-8">
        <Card className="p-4 shadow-md rounded-2xl">
          <CardContent>
            <h2 className="text-xl font-semibold text-green-800 mb-2">Painel do Usuário</h2>
            <p>Saldo Atual: <strong>150.000 AOA</strong></p>
            <p>Lucro Acumulado: <strong>25.000 AOA</strong></p>
            <Button className="mt-4 bg-green-600 hover:bg-green-700">Sacar Lucros</Button>
          </CardContent>
        </Card>
      </section>

      <section className="mb-8">
        <h3 className="text-xl font-semibold text-green-700 mb-4">Histórico de Investimentos</h3>
        <Card className="p-4 shadow-sm rounded-xl">
          <CardContent>
            <ul className="text-sm text-gray-700 space-y-2">
              <li>Plano Pro - 50.000 AOA - 35% - Finalizado</li>
              <li>Plano Start - 25.000 AOA - 15% - Finalizado</li>
              <li>Plano VIP - 100.000 AOA - 50% - Em andamento</li>
            </ul>
          </CardContent>
        </Card>
      </section>

      <section>
        <h3 className="text-xl font-semibold text-green-700 mb-4">Novos Investimentos</h3>
        <Tabs defaultValue="start">
          <TabsList className="grid grid-cols-3 mb-6">
            <TabsTrigger value="start">Plano Start</TabsTrigger>
            <TabsTrigger value="pro">Plano Pro</TabsTrigger>
            <TabsTrigger value="vip">Plano VIP</TabsTrigger>
          </TabsList>

          <TabsContent value="start">
            <InvestmentCard title="Plano Start" amount="25.000 AOA" duration="30 dias" returnRate="15%" />
          </TabsContent>
          <TabsContent value="pro">
            <InvestmentCard title="Plano Pro" amount="50.000 AOA" duration="60 dias" returnRate="35%" />
          </TabsContent>
          <TabsContent value="vip">
            <InvestmentCard title="Plano VIP" amount="100.000 AOA" duration="90 dias" returnRate="50%" />
          </TabsContent>
        </Tabs>
      </section>
    </div>
  );
}

function InvestmentCard({ title, amount, duration, returnRate }) {
  return (
    <Card className="p-4 shadow-md rounded-2xl">
      <CardContent>
        <h2 className="text-2xl font-semibold mb-2 text-green-800">{title}</h2>
        <p className="text-gray-700">Valor: {amount}</p>
        <p className="text-gray-700">Duração: {duration}</p>
        <p className="text-gray-700 mb-4">Retorno: {returnRate}</p>
        <Input placeholder="Número Multicaixa" className="mb-2" />
        <Button className="w-full bg-green-600 hover:bg-green-700">Investir
