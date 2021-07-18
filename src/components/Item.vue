<script>
export default {
  props: {
    value: {},
    name: {},
  },
  render() {
    console.log(this.name);

    return (
      <Input
        value={this.value}
        onInput={($event) => this.$emit("input", $event.target.value)}
      />
    );
  },
};
</script>

<style></style>
