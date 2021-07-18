<script>
const HOC = (Component) => ({
  functional: true,
  render(h, { data }) {
    return (
      <div>
        test
        <Component {...data} />
      </div>
    );
  },
});

// export default {
//   functional: true,
//   props: {
//     value: {},
//     name: {},
//   },
//   render(h, { props, listeners }) {
//     console.log(props.name);

//     return (
//       <Input
//         value={props.value}
//         onInput={($event) => listeners.input($event.target.value)}
//       />
//     );
//   },
// };
export default HOC({
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
});
</script>

<style></style>
