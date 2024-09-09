<script lang='ts'>
    import * as Card from '$lib/components/ui/card';
    import { Button } from '$lib/components/ui/button';
</script>

<div class='w-3/4 mx-auto my-3'>
    <Card.Root class='w-full'>
        <Card.Header>
            <Card.Title>Card Title</Card.Title>
            <Card.Description>Card Description</Card.Description>
        </Card.Header>
        <Card.Content>
            <p>Card Content</p>
        </Card.Content>
        <Card.Footer>
            <p>Card Footer</p>
        </Card.Footer>
    </Card.Root>
</div>
