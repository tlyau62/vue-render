<script>
export default {
  functional: true,
  render(h, { props, listeners }) {
    console.log("Item");
    return (
      <Input
        value={props.value}
        onInput={($event) => {
          listeners.input($event.target.value);
        }}
      />
    );
  },
};
</script>

<style></style>
