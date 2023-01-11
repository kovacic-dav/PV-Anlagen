<template>
  <div>
    <Description
      :foerderungen="foerderungen"
      :investitionsschutz="investitionsschutz"
      :description="description"
    />
    <Requests 
      :headline="headline"
      :data="data"
    />
  </div>
</template>

<script>
import Description from './Description.vue';
import Requests from './Requests.vue';

export default {
  setup() {
    const foerderungen = 'PV - Fördererungen';
    const investitionsschutz = 'EAG-Investitionszuschuss';
    const description =
      'Photovoltaik und Stromspeicher im Jahr 2023 Mit dem Erneuerbaren-Ausbau-Gesetz (EAG) wurden die rechtlichen Rahmenbedingungen für den Netzanschluss von erneuerbaren Energieanlagen vereinfacht. Dies umfasst auch finanzielleErleichterungen in Form eines pauschalierten Netzzutrittsentgelts. Mit einem der EAGInvestitionszuschüsse werden die Neuerrichtung und Erweiterung von Photovoltaikanlagen und die damit verbundene Neuerrichtung von Stromspeichern gefördert. Für die Erweiterung einer Photovoltaikanlage ist keine Mindestgröße vorgesehen.';

    const headline= 'Bisherige Ansuchen (Max. Fördersumme: €1000000)' 
    
    let data = [{
          name: 'Maier',
          plz: '4020',
          zaehlpunkt: '0000-5232-4199-1234-0983',
          kwPeak: 14.4,
          bewilligt: true,
          },
          {
          name: 'Huber',
          plz: '4620',
          zaehlpunkt: '0000-1232-4189-1124-1983',
          kwPeak: 10.0,
          bewilligt: false,
          },
          {
          name: 'Rager',
          plz: '4400',
          zaehlpunkt: '0450-9832-4109-1764-1999',
          kwPeak: 19.0,
          bewilligt: false,
          },
        ]
    return {
      foerderungen,
      investitionsschutz,
      description,
      headline,
      data,
    };
  },
  components: {
    Description,
    Requests,
  },
};
</script>

<style></style>
