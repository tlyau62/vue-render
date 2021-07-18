<script>
import Item from "./Item";

export default {
  props: {
    value: {},
  },
  render() {
    return (
      <div>
        {Object.entries(this.value).map(([k, v]) => (
          <Item
            value={v}
            onInput={($event) => {
              this.$emit("input", { ...this.value, [k]: $event });
            }}
            key={k}
          />
        ))}
      </div>
    );
  },
};
</script>

<style></style>
