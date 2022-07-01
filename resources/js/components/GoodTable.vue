<template>
    <div>
        <vue-good-table
            :columns="columns"
            :rows="rows"
            theme="nocturnal"
            styleClass="vgt-table condensed"            
            
            :search-options="{
                enabled: true,
                placeholder: 'Buscar',
                skipDiacritics: false, // acentuação
            }"

            :pagination-options="{
                enabled: true,
                mode: 'records',
                perPageDropdown: [5, 10, 15, 20],
                jumpFirstOrLast : true,
                firstLabel : '1ª página',
                lastLabel : 'Última página',
                nextLabel: 'Próxima',
                prevLabel: 'Anterior',
                rowsPerPageLabel: 'Resultados por página',
                ofLabel: 'de',
                pageLabel: 'página',
                allLabel: 'Todos',
                zeroRecords: 'ddd'
            }">
            <div slot="table-actions" class="px-2 mt-1">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="#c7ced8" class="bi bi-plus-circle-fill" viewBox="0 0 16 16">
                    <path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM8.5 4.5a.5.5 0 0 0-1 0v3h-3a.5.5 0 0 0 0 1h3v3a.5.5 0 0 0 1 0v-3h3a.5.5 0 0 0 0-1h-3v-3z"/>
                </svg>
            </div>
            <div slot="emptystate">
                Sem registros
            </div>
  
        </vue-good-table>
    </div>
</template>

<script>
export default {
  name: 'my-component',
  data(){
    return {
      columns: [
        {
          label: 'Nome',
          field: 'name',
          thClass: 'bg-dark',
        },
        {
          label: 'Idade',
          field: 'age',
          type: 'number',
        },
        {
          label: 'Criado em',
          field: 'createdAt',
          type: 'date',
          dateInputFormat: 'yyyy-MM-dd',
          dateOutputFormat: 'dd/MM/Y',
        },
        {
          label: 'Porcentagem',
          field: 'score',
          type: 'percentage',
        },
        {
            label: 'Ações',
            field: 'acoes',
            globalSearchDisabled: true,
        }
      ],
      rows: [
        { id:1, name:"ÉEE", age: 20, createdAt: '2022-07-01', score: 0.03343 },
        { id:2, name:"EEE", age: 24, createdAt: '2011-10-31', score: 0.03343 },
        { id:3, name:"Susan", age: 16, createdAt: '2011-10-30', score: 0.03343 },
        { id:4, name:"Chris", age: 55, createdAt: '2011-10-11', score: 0.03343 },
        { id:5, name:"Dan", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        { id:6, name:"John", age: 20, createdAt: '2011-10-31', score: 0.03343 },
        { id:1, name:"ÉEE", age: 20, createdAt: '2022-07-01', score: 0.03343 },
        { id:2, name:"EEE", age: 24, createdAt: '2011-10-31', score: 0.03343 },
        { id:3, name:"Susan", age: 16, createdAt: '2011-10-30', score: 0.03343 },
        { id:4, name:"Chris", age: 55, createdAt: '2011-10-11', score: 0.03343 },
        { id:5, name:"Dan", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        { id:6, name:"John", age: 20, createdAt: '2011-10-31', score: 0.03343 },
        { id:1, name:"ÉEE", age: 20, createdAt: '2022-07-01', score: 0.03343 },
        { id:2, name:"EEE", age: 24, createdAt: '2011-10-31', score: 0.03343 },
        { id:3, name:"Susan", age: 16, createdAt: '2011-10-30', score: 0.03343 },
        { id:4, name:"Chris", age: 55, createdAt: '2011-10-11', score: 0.03343 },
        { id:5, name:"Dan", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        { id:6, name:"John", age: 20, createdAt: '2011-10-31', score: 0.03343 },
        { id:1, name:"ÉEE", age: 20, createdAt: '2022-07-01', score: 0.03343 },
        { id:2, name:"EEE", age: 24, createdAt: '2011-10-31', score: 0.03343 },
        { id:3, name:"Susan", age: 16, createdAt: '2011-10-30', score: 0.03343 },
        { id:4, name:"Chris", age: 55, createdAt: '2011-10-11', score: 0.03343 },
        { id:5, name:"Dan", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        { id:6, name:"John", age: 20, createdAt: '2011-10-31', score: 0.03343 },
        { id:1, name:"ÉEE", age: 20, createdAt: '2022-07-01', score: 0.03343 },
        { id:2, name:"EEE", age: 24, createdAt: '2011-10-31', score: 0.03343 },
        { id:3, name:"Susan", age: 16, createdAt: '2011-10-30', score: 0.03343 },
        { id:4, name:"Chris", age: 55, createdAt: '2011-10-11', score: 0.03343 },
        { id:5, name:"Dan", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        { id:6, name:"John", age: 20, createdAt: '2011-10-31', score: 0.03343 },
        { id:1, name:"ÉEE", age: 20, createdAt: '2022-07-01', score: 0.03343 },
        { id:2, name:"EEE", age: 24, createdAt: '2011-10-31', score: 0.03343 },
        { id:3, name:"Susan", age: 16, createdAt: '2011-10-30', score: 0.03343 },
        { id:4, name:"Chris", age: 55, createdAt: '2011-10-11', score: 0.03343 },
        { id:5, name:"Dan", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        { id:6, name:"John", age: 20, createdAt: '2011-10-31', score: 0.03343 },
      ],
    };
  },
};
</script>