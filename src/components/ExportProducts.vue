<template>
  <Vueform validate-on="step|change" endpoint="http://form.karantin.uz/api/v1/save" method="POST"
    add-class="vf-export-products">

    <StaticElement name="karantinuz" tag="img"
      src="https://play-lh.googleusercontent.com/4ZdETydyfS7bP-ZvNEJVruc26KTcBXxfglSbvU3ueKDyQGY1fPgn_j-ZSO3yGIM3wMM=w240-h480-rw"
      align="center" size="md" />

    <StaticElement name="title" tag="h4"
      content="Ўзбекистон мева-сабзавотларининг хорижий бозорлардаги ўртача нархлари тўғрисида" align="center" />

    <GroupElement name="container">
      <SelectElement name="Давлат" label="Davlat" info="tanlang!" :items="[
        {
          value: 'Озарбайжон',
          label: 'Озарбайжон',
        },
        {
          value: 'Буюк Британия',
          label: 'Буюк Британия',
        },
      ]" />
      <SelectElement name="Maxsulot turi" label="Маҳсулот номи (таржима)" info="tanlang!" :items="[
        {
          value: 'Янги узилган помидор',
          label: 'Янги узилган помидор',
        },
        {
          value: 'Янги пиёз',
          label: 'Янги пиёз',
        },
      ]" :rules="[
        'required',
      ]" />
      <TextElement name="Navi" label="Нави" :rules="[
        'required',
      ]" />
      <TextElement name="Qadog'i" label="Қадоғи" :rules="[
        'required',
      ]" />
      <StaticElement name="divider" tag="hr" />
      <StaticElement name="h4" tag="h4" content="Савдо тармоқларидаги нарх" align="center" />
      <StaticElement name="p" tag="p" content="1 кг учун, АҚШ долларида" align="left" size="md" />
      <GroupElement name="prices">
        <GroupElement name="column1" :columns="{
        container: 4,
      }">
          <TextElement name="savda_tarmoq_min" label="энг паст" size="sm" field-name="энг паст" :rules="[
        'required',
      ]" :columns="{
        container: 7,
      }" />
        </GroupElement>
        <GroupElement name="column2" :columns="{
        container: 4,
      }">
          <TextElement name="savda_tarmoq_mid" label="ўртача" size="sm" field-name="энг паст" :rules="[
        'required',
      ]" :columns="{
        container: 7,
      }" />
        </GroupElement>
        <GroupElement name="column3" :columns="{
        container: 4,
      }">
          <TextElement name="savda_tarmoq_max" label="энг баланд" size="sm" field-name="энг паст" :rules="[
        'required',
        'min:1',
        'max:100000000',
        'regex:^\\d',
      ]" :columns="{
        container: 7,
      }" />
        </GroupElement>
      </GroupElement>
      <StaticElement name="divider_copy" tag="hr" />
      <StaticElement name="h4_copy" tag="h4" content="Бозордаги нарх" align="center" />
      <StaticElement name="p_copy" tag="p" content="1 кг учун, АҚШ долларида" align="left" size="md" />
      <GroupElement name="prices_copy">
        <GroupElement name="column1" :columns="{
        container: 4,
      }">
          <TextElement name="market_price_min" label="энг паст" size="sm" field-name="энг паст" :rules="[
        'required',
      ]" :columns="{
        container: 7,
      }" />
        </GroupElement>
        <GroupElement name="column2" :columns="{
        container: 4,
      }">
          <TextElement name="market_price_mid" label="ўртача" size="sm" field-name="энг паст" :rules="[
        'required',
      ]" :columns="{
        container: 7,
      }" />
        </GroupElement>
        <GroupElement name="column3" :columns="{
        container: 4,
      }">
          <TextElement name="market_price_max" label="энг баланд" size="sm" field-name="энг паст" :rules="[
        'required',
        'min:1',
        'max:100000000',
        'regex:^\\d',
      ]" :columns="{
        container: 7,
      }" />
        </GroupElement>
      </GroupElement>
    </GroupElement>
    <ButtonElement name="submit" button-label="Submit" :submits="true" align="right" size="md" :full="true" />
  </Vueform>
</template>

